---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 49c3fa6ec85f97c3c4010b6cfc9282933a844a6e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276838"
---
# <span data-ttu-id="c4158-101">Update-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="c4158-101">Update-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="c4158-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4158-102">SYNOPSIS</span></span>
<span data-ttu-id="c4158-103">Azure Site Recovery koruma kapsayıcısı eşlemesini güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="c4158-103">Update the Azure site recovery protection container mapping.</span></span>

## <span data-ttu-id="c4158-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c4158-104">SYNTAX</span></span>

### <span data-ttu-id="c4158-105">AzureToAzureEnableAutoUpdate (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c4158-105">AzureToAzureEnableAutoUpdate (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-AzureToAzure] [-EnableAutoUpdate] -AutomationAccountId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4158-106">AzureToAzureDisableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="c4158-106">AzureToAzureDisableAutoUpdate</span></span>
```
Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-AzureToAzure] [-DisableAutoUpdate] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c4158-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c4158-107">DESCRIPTION</span></span>
<span data-ttu-id="c4158-108">**Update-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet 'i, belirtilen Azure Site Recovery koruma kapsayıcısı eşlemesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c4158-108">The **Update-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet updates the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="c4158-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c4158-109">EXAMPLES</span></span>

### <span data-ttu-id="c4158-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c4158-110">Example 1</span></span>
```powershell
PS C:> Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject $ASRProtectionContainerMapping -AzureToAzure -DisableAutoUpdate
```

<span data-ttu-id="c4158-111">Kapsayıcıyı otomatik güncelleştirmeyi devre dışı bırakmak için işlemi başlatın.</span><span class="sxs-lookup"><span data-stu-id="c4158-111">Start the operation to disable auto update for container.</span></span>

### <span data-ttu-id="c4158-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="c4158-112">Example 2</span></span>
```powershell
PS C:> Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject $ASRProtectionContainerMapping  -AzureToAzure -EnableAutoUpdate -AutomationAccountId $automationAccountId
```

<span data-ttu-id="c4158-113">Kapsayıcıyı otomatik güncelleştirmeyi etkinleştir özelliğini devre dışı bırakmak için işlemi başlatın.</span><span class="sxs-lookup"><span data-stu-id="c4158-113">Start the operation to disable enable auto update for container.</span></span>

## <span data-ttu-id="c4158-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c4158-114">PARAMETERS</span></span>

### <span data-ttu-id="c4158-115">-Automationaccountıd</span><span class="sxs-lookup"><span data-stu-id="c4158-115">-AutomationAccountId</span></span>
<span data-ttu-id="c4158-116">Otomatik UDPATE kullanılan Otomasyon hesap kimliği 'ni belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4158-116">Specifies the automation accountId used for auto udpate.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureEnableAutoUpdate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4158-117">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="c4158-117">-AzureToAzure</span></span>
<span data-ttu-id="c4158-118">Azure to Azure Protection kapsayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4158-118">Specifies Azure to Azure protection container.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4158-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4158-119">-DefaultProfile</span></span>
<span data-ttu-id="c4158-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c4158-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4158-121">-Disableotomatik güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="c4158-121">-DisableAutoUpdate</span></span>
<span data-ttu-id="c4158-122">Otomatik güncelleştirmeyi devre dışı bırakmak için parametreyi değiştirin.</span><span class="sxs-lookup"><span data-stu-id="c4158-122">Switch parameter to disable auto update.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzureDisableAutoUpdate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4158-123">-Enableotomatik güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="c4158-123">-EnableAutoUpdate</span></span>
<span data-ttu-id="c4158-124">Otomatik güncelleştirmeyi etkinleştirmek için parametre değiştirme.</span><span class="sxs-lookup"><span data-stu-id="c4158-124">Switch parameter to enable auto update.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzureEnableAutoUpdate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4158-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4158-125">-InputObject</span></span>
<span data-ttu-id="c4158-126">Koruma kapsayıcısı eşleme nesnesi.</span><span class="sxs-lookup"><span data-stu-id="c4158-126">Object for protection container mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: ProtectionContainerMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4158-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="c4158-127">-Confirm</span></span>
<span data-ttu-id="c4158-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c4158-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4158-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4158-129">-WhatIf</span></span>
<span data-ttu-id="c4158-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c4158-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4158-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c4158-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4158-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4158-132">CommonParameters</span></span>
<span data-ttu-id="c4158-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c4158-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4158-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c4158-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4158-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c4158-135">INPUTS</span></span>

### <span data-ttu-id="c4158-136">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="c4158-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="c4158-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c4158-137">OUTPUTS</span></span>

### <span data-ttu-id="c4158-138">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c4158-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c4158-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c4158-139">NOTES</span></span>

## <span data-ttu-id="c4158-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c4158-140">RELATED LINKS</span></span>
