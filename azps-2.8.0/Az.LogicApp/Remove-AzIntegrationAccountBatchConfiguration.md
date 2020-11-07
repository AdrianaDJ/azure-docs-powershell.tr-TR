---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: e2c4f3f399bd4bcd472ae04c6ca2234c2d2b26d2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751511"
---
# <span data-ttu-id="0d1c6-101">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="0d1c6-101">Remove-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="0d1c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d1c6-102">SYNOPSIS</span></span>
<span data-ttu-id="0d1c6-103">Tümleştirme hesabı toplu yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0d1c6-103">Removes an integration account batch configuration.</span></span>

## <span data-ttu-id="0d1c6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0d1c6-104">SYNTAX</span></span>

### <span data-ttu-id="0d1c6-105">Byıntegrationaccount (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0d1c6-105">ByIntegrationAccount (Default)</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d1c6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0d1c6-106">ByInputObject</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d1c6-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="0d1c6-107">ByResourceId</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d1c6-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0d1c6-108">DESCRIPTION</span></span>
<span data-ttu-id="0d1c6-109">**Remove-Azıntegrationaccountbatchconfiguration** cmdlet 'i, tümleştirme hesabından toplu iş yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0d1c6-109">The **Remove-AzIntegrationAccountBatchConfiguration** cmdlet removes a batch configuration from an integration account.</span></span>

## <span data-ttu-id="0d1c6-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0d1c6-110">EXAMPLES</span></span>

### <span data-ttu-id="0d1c6-111">Örnek 1: parametrelere göre bir toplu iş yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="0d1c6-111">Example 1: Remove a batch configuration by parameters</span></span>
```powershell
PS C:\> Remove-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig"
```

<span data-ttu-id="0d1c6-112">"Sampleıntegrationaccount" tümleştirme hesabında bulunan "sampleBatchConfig" adlı toplu iş yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0d1c6-112">Removes the batch configuration named "sampleBatchConfig" located in the integration account "sampleIntegrationAccount".</span></span>

## <span data-ttu-id="0d1c6-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0d1c6-113">PARAMETERS</span></span>

### <span data-ttu-id="0d1c6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d1c6-114">-DefaultProfile</span></span>
<span data-ttu-id="0d1c6-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0d1c6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d1c6-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d1c6-116">-InputObject</span></span>
<span data-ttu-id="0d1c6-117">Tümleştirme hesabı toplu iş yapılandırması.</span><span class="sxs-lookup"><span data-stu-id="0d1c6-117">An integration account batch configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d1c6-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="0d1c6-118">-Name</span></span>
<span data-ttu-id="0d1c6-119">Tümleştirme hesabı toplu işlem yapılandırma adı.</span><span class="sxs-lookup"><span data-stu-id="0d1c6-119">The integration account batch configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: BatchConfigurationName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d1c6-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="0d1c6-120">-ParentName</span></span>
<span data-ttu-id="0d1c6-121">Tümleştirme hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="0d1c6-121">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d1c6-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="0d1c6-122">-PassThru</span></span>
<span data-ttu-id="0d1c6-123">Komutun başarılı olup olmadığını döndürün.</span><span class="sxs-lookup"><span data-stu-id="0d1c6-123">Return whether the command was successful or not.</span></span>

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

### <span data-ttu-id="0d1c6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d1c6-124">-ResourceGroupName</span></span>
<span data-ttu-id="0d1c6-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="0d1c6-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d1c6-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0d1c6-126">-ResourceId</span></span>
<span data-ttu-id="0d1c6-127">Tümleştirme hesabı toplu yapılandırması kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="0d1c6-127">The integration account batch configuration resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d1c6-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="0d1c6-128">-Confirm</span></span>
<span data-ttu-id="0d1c6-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0d1c6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d1c6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d1c6-130">-WhatIf</span></span>
<span data-ttu-id="0d1c6-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0d1c6-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0d1c6-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0d1c6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d1c6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d1c6-133">CommonParameters</span></span>
<span data-ttu-id="0d1c6-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0d1c6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d1c6-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d1c6-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d1c6-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0d1c6-136">INPUTS</span></span>

### <span data-ttu-id="0d1c6-137">Microsoft. Azure. Commands. Logicuyg. modeller. Psıntegrationaccountbatchconfiguration</span><span class="sxs-lookup"><span data-stu-id="0d1c6-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

### <span data-ttu-id="0d1c6-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0d1c6-138">System.String</span></span>

## <span data-ttu-id="0d1c6-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0d1c6-139">OUTPUTS</span></span>

### <span data-ttu-id="0d1c6-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0d1c6-140">System.Boolean</span></span>

## <span data-ttu-id="0d1c6-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0d1c6-141">NOTES</span></span>

## <span data-ttu-id="0d1c6-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0d1c6-142">RELATED LINKS</span></span>