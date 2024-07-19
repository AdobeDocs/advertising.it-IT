---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---
# Campo Tipo di reindirizzamento nelle impostazioni dell’account e della campagna

**[!UICONTROL Redirect Type]:** (solo per [!UICONTROL EF Redirect]) metodo di reindirizzamento degli utenti finali all&#39;URL finale o di destinazione. L’opzione selezionata è applicabile a tutti gli annunci, le parole chiave e i posizionamenti nell’account o nella campagna. L&#39;impostazione predefinita a livello di account viene ereditata dalle impostazioni di tracciamento dell&#39;inserzionista e l&#39;impostazione predefinita a livello di campagna viene ereditata dalle impostazioni dell&#39;account.

* *[!UICONTROL Standard]:* Per reindirizzare l&#39;utente finale all&#39;URL specificato.

* *[!UICONTROL Token]:* Per reindirizzare l&#39;utente finale all&#39;URL e registrare anche l&#39;ID Search, Social e Commerce per il clic (`ef_id`) come parametro della stringa di query, utilizzato come token. Scegliere questa opzione se si desidera creare rapporti sulle transazioni non in linea, se si desidera che Search, Social e Commerce scambino dati con Adobe Analytics o se si desidera tenere traccia di tutte le conversioni che si verificano nei browser [!DNL Apple Safari].

**Note:**

* Se passi da [!UICONTROL Standard] a [!UICONTROL Token] o viceversa, devi rigenerare gli URL di tracciamento per l&#39;account.
* Puoi sovrascrivere l’impostazione a livello di account a livello di campagna.
