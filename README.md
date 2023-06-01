# EU_MDR_bolus-sim
>.On the EU Medical Device Regulations >(EU 2017/745) - Insulin pumps with >bolus calculator


Hello world,

This repository is created to support all parties involved in so-called insulin pump bolus calculators, specifically but not exclusively those available in The Netherlands (the 'EU'). The information in this repository is for educational purposes only.

All devices discussed in this repository are subject to strict regulations.[1] Manufacturers must perform extensive testing procedures before a release on the market is allowed. Yet, miscalculations of the bolus calculator are not unheard of.[2] Miscalculation of a bolus may result in the user administering an incorrect dose of insulin. This may cause harm and even death of the user.[3] Adequate documentation of the specifications of such calculations [in the instructions for use] is therefore of great importance for validation purposes. Users and healthcare providers must be able to confirm whether or not the device works as intended, at all times.

Preliminary screening of the available documentation for 11 devices shows that improvements must be made.[4] All reviewed system user guides (instructions for use; gebruiksaanwijzing [NL]) provide either incomplete or incorrect or ambiguous specifications. During further investigation, it appeared that providing adequate specifications of the bolus calculator seemed not to be a matter of priority for most manufacturers.[5]

According to EU MDR (EU 2017/745) Chapter III 23.1, if manufacturer has a website, then manufacturer shall make required device information available on the website. All manufacturers of reviewed devices have a website.[6]

When manufacturers were contacted for clarification, of only one device the requested specifications were provided within acceptable timeframe (days, weeks). Of one manufacturer, a clarification (for all devices) was received after >1 year, but only after an escalation cascade was introduced. For none of the other devices the requested specifications were provided, nor have updates been released of the system user guide.[7]

To protect the users against possible incompliance of manufacturers and healthcare providers, and to protect manufacturers and healthcare providers against possible incompetence of consultants and research firms, methods have been tested and applied to detect certain forms of incompliance and incompetence. These methods are discussed in later reports, available in this repository for free. After all, high quality doesn't necessarily involve high costs, if one understands the essence of what is and what is not.[8]


For example:

EU MDR (EU 2017/745), article II definitions, (1), classifies software that is used in the treatment of disease as a medical device. This means that software that performs calculations that are used in the treatment of disease is a medical device. Article 23.4, (k), states that the instructions for use shall then contain (amongst others) the information needed to verify whether the device is properly installed and is ready to perform safely 
and as intended by the manufacturer. 

It must be noted that due the proprietary nature of most software classified as a medical device, that this information is almost never available to the user. Provided there is physical access to the device or system, it is possible to reverse-engineer and obtain the required files/code, e.g. from the ROM file of an insulin pump handheld device, but this is not a skill widespread among the general population. Proprietary software may also not be written in clear language, i.e. in a manner allowing it to be understood by users, making it difficult to decipher and validate even when successfully accessed. It is therefore usually not possible for the user to confirm whether or not such software is properly installed. This raises a compliance issue for not only insulin pumps, but for numerous other medical devices as well.[9]

Have you been advised by a consultant or research firm about the new EU MDR (EU 2017/745), then please mind that if you have not been made aware of this possible compliance issue, that you have been inadequately informed. It might be wise to review the work of the consultant or research firm in question, to ensure that other possible compliance issues have not gone unnoticed. 

--------------------------------

A well-informed consultant would, for example, have advised to start developing the means to provide information to the user about the installation of the software, so that the code can largely remain as it is / no major changes would have to be introduced to the software itself, at least for the time being. 
A well-informed consultant would also have contacted a regulatory authority and/or a government information office to request clarification, to which a reply would have been received that provides no insight at all, after which could be concluded that the new EU MDR might have consequences of which almost none are fully aware, or none have been made aware, which gives client(s) time to think and possibly introduce upgrades to devices currently in development or on the drawing table.

----

Are you a consultant that informed your client(s) of the above mentioned before the date of 3 September 2021, then feel free to email us at 
repository@boluscalculators.com, so that we may verify and spread the word of your consulting qualities.

Are you a user of one of the medical devices reviewed in this repository, then of course for any inquiries, suggestions, complaints, et cetera, do not hesitate to contact us. We are not allowed to provide medical assistance, but we can possibly open doors that you cannot. This service is for free: users@boluscalculators.com

Are you any other party that feels the need to contact us, please also feel free to do so via repository@boluscalculators.com

To add device for review --> 
Provide manufacturer name and device model to devices@boluscalculators.com, and we will take a keen look at the device and its manufacturer's procedures.

For other/custom testing services, please contact: toolmaster [at] boluscalculators dot com.

These services are for free / privately funded. If an exception arises, e.g. an extremely high cost due to the nature of your inquiry, then you will be informed of the specifics.

--------------------------------


#Preliminary report / cable

Some things to be aware of:

With the exception of $DEVICE5 (.manufacturer_2), none of the manufacturers listed below provided insight in the workings of their bolus calculator for over a year after the first (of several) inquiries.

//

Of .manufacturer_1 ($NAME), the bolus calculator specifications are available in the system user guides of all devices, but for the third iteration ($DEVICE3) the bolus calculator specifications may differ depending on what language of the system user guide is used. This concerns specifically the rounding of results, which is described in several languages as "rounded to the nearest 0.5", while in other languages it reads "rounded down to the nearest 0.5". According to these system user guides, the same device calculates differently depending on the country where it is acquired and/or the language of the user, which is incorrect (the calculations are the same for all countries/languages). The correct specifications have been obtained unofficially / via a backdoor. These specifications have been 'confirmed' by testing the bolus calculator on different devices with different language settings. Officially, this manufacturer still provides wrong specifications to the users in The Netherlands, Belgium, and Germany for the third iteration device.
#the correct specification for the rounding of results for $DEVICE3 is that the results of all bolus calculations are rounded down to the nearest (multiple of) 0.05 units of insulin.

Of .manufacturer_2 ($NAME), the bolus calculator specifications in the system user guides are incomplete for both devices. However, for $DEVICE4 the missing specifications were provided immediately by the Dutch product support unit upon inquiry. These specifications are in great detail. Their reply is exemplary for all others. For $DEVICE5 (UK) the specifications remain incomplete. The product support unit failed to understand the question and had more attention to our home address that was required to be filled in their contact webform. It appears that no users are registered in SW1A 0AA London. The value "active insulin" that is used in some of the calculations remains unspecified for $DEVICE5.
#the specification of the value "active insulin" for $DEVICE4 is as follows: IMG

Of .manufacturer_3 ($NAME), in all system user guides that include an image of bolus formula ## in the system user guide, the specifications are ambiguous. The formula in the image differs from the formula in the text. This manufacturer's product support unit could initially not be reached via the channels as stated on their website. An escalation cascade was used in order to obtain the required information. A reply was received to the inquiry of last year on the specifications of the bolus calculator (...). These specifications are now unambiguous and complete. The simulators of the devices listed under .manufacturer_3 are therefore under construction. 
#the correct specifications for bolus formula ## are as follows: IMG

Of .manufacturer_4 ($NAME), the bolus calculator specifications are entirely absent in the system user guide of $DEVICE10, nor are they available on the website. The product support unit of this manufacturer failed to understand the question and the importance of the matter. The inquiry was eventually forwarded to the "Security Officer", after which all communication ceased. Almost directly after inquiring, the system user guide was temporarily unavailable on the website. Later, the system user guide was revised but unfortunately still lacks any specifications of the bolus calculations. None of our inquiries have been answered with the required information (bolus calculations)
#Please mind that this manufacturer had its system breached and user data accessed by an unknown actor in Jan 2020. The manufacturer has since then raised its defenses, and this is affecting communication with the outside world.

Of .manufacturer_5 ($NAME), the bolus calculator specifications are entirely absent in the system user guide of $DEVICE11, nor are they available on the website. A reply was received to an inquiry of last year, that an update was in the making for the website, but to this day no specifications are available. It must be noted however that the reply of the this manufacturer's product support unit was immediate and with good intentions on all occasions. The website has been updated with more information since then. In that sense, this manufacturer's product support unit is second best (.manufacturer_2 [NL] being the winner).



--------------------------------
>
>.Categories: Multidisciplinary, not elsewhere classified
>
>.Types: Document research, format and prototype development, device validation
>
>.Funding: Private
>
>.Timeline: Ongoing
>
--------------------------------

>.[1] $SOURCE_1
>
>.[2] $SOURCE_2
>
>.[3] $SOURCE_3
>
>.[4] $SOURCE_4
>
>.[5] $SOURCE_5
>
>.[6] $SOURCE_6
>
>.[7] $SOURCE_7
>
>.[8] $SOURCE_8
>
>.[9] $SOURCE_9

--------------------------------

End of introduction
