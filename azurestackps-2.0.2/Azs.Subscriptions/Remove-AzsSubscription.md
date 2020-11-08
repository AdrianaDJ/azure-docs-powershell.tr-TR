---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscriptions/remove-azssubscription
schema: 2.0.0
ms.openlocfilehash: b6fddf677cd619dad577b7bca8286671b85d0791
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94107021"
---
# <span data-ttu-id="7bb91-101">Remove-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="7bb91-101">Remove-AzsSubscription</span></span>

## <span data-ttu-id="7bb91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bb91-102">SYNOPSIS</span></span>


## <span data-ttu-id="7bb91-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7bb91-103">SYNTAX</span></span>

### <span data-ttu-id="7bb91-104">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7bb91-104">Delete (Default)</span></span>
```
Remove-AzsSubscription -SubscriptionId <String> [-DefaultProfile <PSObject>] [-Force] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7bb91-105">Deleteviaıdentity</span><span class="sxs-lookup"><span data-stu-id="7bb91-105">DeleteViaIdentity</span></span>
```
Remove-AzsSubscription -InputObject <ISubscriptionIdentity> [-DefaultProfile <PSObject>] [-Force] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7bb91-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="7bb91-106">DESCRIPTION</span></span>


## <span data-ttu-id="7bb91-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7bb91-107">EXAMPLES</span></span>

### <span data-ttu-id="7bb91-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7bb91-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzsSubscription -SubscriptionId d387f779-85d8-40b6-8607-8306295ebff9

```

<span data-ttu-id="7bb91-109">Belirtilen aboneliği silin.</span><span class="sxs-lookup"><span data-stu-id="7bb91-109">Delete the specifed subscription.</span></span>

## <span data-ttu-id="7bb91-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7bb91-110">PARAMETERS</span></span>

### <span data-ttu-id="7bb91-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bb91-111">-DefaultProfile</span></span>


```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7bb91-112">-Force</span><span class="sxs-lookup"><span data-stu-id="7bb91-112">-Force</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7bb91-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7bb91-113">-InputObject</span></span>
<span data-ttu-id="7bb91-114">Oluşturmak için, ıNPUTOBJECT özelliklerinin Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7bb91-114">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="7bb91-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="7bb91-115">-PassThru</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7bb91-116">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="7bb91-116">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7bb91-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="7bb91-117">-Confirm</span></span>
<span data-ttu-id="7bb91-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7bb91-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7bb91-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bb91-119">-WhatIf</span></span>
<span data-ttu-id="7bb91-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7bb91-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bb91-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7bb91-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7bb91-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bb91-122">CommonParameters</span></span>
<span data-ttu-id="7bb91-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7bb91-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bb91-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7bb91-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bb91-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7bb91-125">INPUTS</span></span>

### <span data-ttu-id="7bb91-126">Microsoft. Azure. PowerShell. cmdlet. Subscription. modeller. ıubscriptionıdentity</span><span class="sxs-lookup"><span data-stu-id="7bb91-126">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.ISubscriptionIdentity</span></span>

## <span data-ttu-id="7bb91-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7bb91-127">OUTPUTS</span></span>

### <span data-ttu-id="7bb91-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7bb91-128">System.Boolean</span></span>



## <span data-ttu-id="7bb91-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7bb91-129">NOTES</span></span>

<span data-ttu-id="7bb91-130">KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7bb91-130">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7bb91-131">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7bb91-131">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="7bb91-132">INPUTOBJECT <ISubscriptionIdentity> :</span><span class="sxs-lookup"><span data-stu-id="7bb91-132">INPUTOBJECT <ISubscriptionIdentity>:</span></span> 
  - <span data-ttu-id="7bb91-133">`[DelegatedProviderId <String>]`: Temsilci seçilen sağlayıcının kimliği.</span><span class="sxs-lookup"><span data-stu-id="7bb91-133">`[DelegatedProviderId <String>]`: Id of the delegated provider.</span></span>
  - <span data-ttu-id="7bb91-134">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="7bb91-134">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7bb91-135">`[OfferName <String>]`: Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="7bb91-135">`[OfferName <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="7bb91-136">`[SubscriptionId <String>]`: Aboneliğin kimliği.</span><span class="sxs-lookup"><span data-stu-id="7bb91-136">`[SubscriptionId <String>]`: Id of the subscription.</span></span>

## <span data-ttu-id="7bb91-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7bb91-137">RELATED LINKS</span></span>

