# Swire Coca-Cola Predictive Maintenance Project

## Business Problem

Swire Coca-Cola currently experiences annual losses of approximately $60 million due to machine downtime, driven by a reactive maintenance strategy that deploys workers only after breakdowns occur. This reactive approach limits productivity and hinders the company’s ability to meet demand. Addressing this issue requires a predictive solution capable of identifying machines likely to fail before they malfunction, reducing downtime and increasing operational efficiency.

## Benefit of the Solution

The proposed solution involves developing a machine learning-based predictive maintenance model. By leveraging historical data from Swire Coca-Cola’s Integrated Work Control (IWC) system, the model can forecast which machines are most likely to fail. This enables the company to stock necessary parts in advance and schedule preemptive repairs, minimizing downtime and ensuring production schedules remain uninterrupted. The solution also offers the potential to lower operational expenses by optimizing staffing needs and reducing emergency repair costs.

## Success Metrics

The success of this project will be determined by its ability to achieve:

A reduction in downtime, which will translate to increased production capacity.
A reduction in maintenance costs, lowering operational expenses.
Improved productivity and Swire Coca-Cola's ability to meet consumer demand.

## Analytics Approach

Our team proposed creating a predictive maintenance model using machine learning techniques trained on historical IWC system data. The model integrates features such as machine location, part descriptions, failure types, and repair times to predict time-to-failure for individual machines. The model’s output will be integrated into a real-time dashboard, providing plant managers with actionable insights and enabling them to proactively schedule maintenance and stock necessary parts.

## Scope

The project aims to deliver:

A predictive maintenance model capable of identifying machines at high risk of failure.
Additional graphs and insights drawn from the data.

## Exploratory Data Analysis (EDA) Insights
The EDA phase revealed critical insights about plant operations and the dataset’s structure:

High-impact plants: Some plants, such as Plant G261, showed the highest volume of maintenance activities, making them prime candidates for targeted interventions.
![image](https://github.com/user-attachments/assets/21d2fb8d-046f-4b60-89e7-ce9fdd56654b)

Unplanned maintenance: Equipment frequently associated with unplanned maintenance events, such as specific equipment IDs, were identified.
![image](https://github.com/user-attachments/assets/756a76ee-2f76-40f5-b514-732f32f83ff1)

Missing data: Significant data gaps were observed, with some columns missing over 70% of their values. A subset of reliable data was isolated for further modeling.
![image](https://github.com/user-attachments/assets/5d7200ac-5573-4756-b400-0acd46f77285)

Key variables: Metrics like average repair times and failure frequency provided foundational insights for developing target variables, such as "Time to Failure."

## Data Preparation

Preparing the dataset for modeling involved:

Handling missing values: Key columns were imputed where possible, while rows with insufficient data were removed.

Feature engineering: New variables, such as "Time to Failure" and "Days Since Planned Maintenance," were calculated to capture failure likelihoods more effectively.

Chronological sorting: Data was arranged by machine and timestamp to ensure the integrity of time-based predictions.

## Modeling

The predictive maintenance model used survival analysis, specifically Kaplan-Meier survival curves, to calculate time-to-failure for machines. Two survival models were developed:

Machine-level survival, analyzing the time between unplanned maintenance events.

Equipment-level survival, focusing on specific components within machines.

The models achieved concordance indices of 0.78 and 0.76, indicating good predictive accuracy. These metrics demonstrate the potential to forecast breakdowns and proactively schedule maintenance.

## Insights and Recommendations

The modeling process yielded actionable insights:

Machines and components with the highest risk of failure were identified, enabling targeted preventive actions.

Maintenance schedules can now be optimized based on calculated survival times, reducing unplanned downtime.

By integrating predictive outputs into a dashboard, Swire Coca-Cola can improve repair efficiency and reduce overall costs.
![image](https://github.com/user-attachments/assets/e82f6191-d445-4af4-989e-6bc2c9634efc)


## Limitations and Opportunities

While the models performed well, the project faced challenges due to:

Extensive missing data, limiting the scope of some analyses.

A lack of real-time machine telemetry data, such as temperature or pressure, which could enhance model precision.

Future opportunities include incorporating additional features, such as live sensor data, and refining the data collection process to reduce gaps.

## Conclusion

The Swire Coca-Cola Predictive Maintenance project successfully demonstrated the potential of machine learning to address a critical operational challenge. By shifting from a reactive to a predictive approach, our team laid the groundwork for reduced downtime, increased productivity, and improved cost-efficiency. With further refinement and data collection, the predictive maintenance system promises to become a cornerstone of Swire Coca-Cola’s operational strategy.

