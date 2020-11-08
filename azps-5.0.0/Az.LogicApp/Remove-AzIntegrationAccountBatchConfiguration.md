---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 848ce0e0c5608271f1f8facb955aad2df95b6a0a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280130"
---
# <span data-ttu-id="f6a76-101">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f6a76-101">Remove-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="f6a76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6a76-102">SYNOPSIS</span></span>
<span data-ttu-id="f6a76-103">Tümleştirme hesabı toplu yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f6a76-103">Removes an integration account batch configuration.</span></span>

## <span data-ttu-id="f6a76-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f6a76-104">SYNTAX</span></span>

### <span data-ttu-id="f6a76-105">Byıntegrationaccount (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f6a76-105">ByIntegrationAccount (Default)</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6a76-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f6a76-106">ByInputObject</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6a76-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="f6a76-107">ByResourceId</span></span>
```
Remove-AzIntegrationAccountBatchConfiguration -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6a76-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f6a76-108">DESCRIPTION</span></span>
<span data-ttu-id="f6a76-109">**Remove-Azıntegrationaccountbatchconfiguration** cmdlet 'i, tümleştirme hesabından toplu iş yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f6a76-109">The **Remove-AzIntegrationAccountBatchConfiguration** cmdlet removes a batch configuration from an integration account.</span></span>

## <span data-ttu-id="f6a76-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f6a76-110">EXAMPLES</span></span>

### <span data-ttu-id="f6a76-111">Örnek 1: parametrelere göre bir toplu iş yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="f6a76-111">Example 1: Remove a batch configuration by parameters</span></span>
```powershell
PS C:\> Remove-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig"
```

<span data-ttu-id="f6a76-112">"Sampleıntegrationaccount" tümleştirme hesabında bulunan "sampleBatchConfig" adlı toplu iş yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f6a76-112">Removes the batch configuration named "sampleBatchConfig" located in the integration account "sampleIntegrationAccount".</span></span>

## <span data-ttu-id="f6a76-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f6a76-113">PARAMETERS</span></span>

### <span data-ttu-id="f6a76-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6a76-114">-DefaultProfile</span></span>
<span data-ttu-id="f6a76-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f6a76-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6a76-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6a76-116">-InputObject</span></span>
<span data-ttu-id="f6a76-117">Tümleştirme hesabı toplu iş yapılandırması.</span><span class="sxs-lookup"><span data-stu-id="f6a76-117">An integration account batch configuration.</span></span>

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

### <span data-ttu-id="f6a76-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="f6a76-118">-Name</span></span>
<span data-ttu-id="f6a76-119">Tümleştirme hesabı toplu işlem yapılandırma adı.</span><span class="sxs-lookup"><span data-stu-id="f6a76-119">The integration account batch configuration name.</span></span>

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

### <span data-ttu-id="f6a76-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="f6a76-120">-ParentName</span></span>
<span data-ttu-id="f6a76-121">Tümleştirme hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="f6a76-121">The integration account name.</span></span>

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

### <span data-ttu-id="f6a76-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f6a76-122">-PassThru</span></span>
<span data-ttu-id="f6a76-123">Komutun başarılı olup olmadığını döndürün.</span><span class="sxs-lookup"><span data-stu-id="f6a76-123">Return whether the command was successful or not.</span></span>

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

### <span data-ttu-id="f6a76-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6a76-124">-ResourceGroupName</span></span>
<span data-ttu-id="f6a76-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f6a76-125">The resource group name.</span></span>

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

### <span data-ttu-id="f6a76-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f6a76-126">-ResourceId</span></span>
<span data-ttu-id="f6a76-127">Tümleştirme hesabı toplu yapılandırması kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="f6a76-127">The integration account batch configuration resource id.</span></span>

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

### <span data-ttu-id="f6a76-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="f6a76-128">-Confirm</span></span>
<span data-ttu-id="f6a76-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f6a76-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6a76-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6a76-130">-WhatIf</span></span>
<span data-ttu-id="f6a76-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f6a76-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f6a76-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f6a76-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6a76-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6a76-133">CommonParameters</span></span>
<span data-ttu-id="f6a76-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f6a76-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6a76-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6a76-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6a76-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f6a76-136">INPUTS</span></span>

### <span data-ttu-id="f6a76-137">Microsoft. Azure. Commands. Logicuyg. modeller. Psıntegrationaccountbatchconfiguration</span><span class="sxs-lookup"><span data-stu-id="f6a76-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

### <span data-ttu-id="f6a76-138">System. String</span><span class="sxs-lookup"><span data-stu-id="f6a76-138">System.String</span></span>

## <span data-ttu-id="f6a76-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f6a76-139">OUTPUTS</span></span>

### <span data-ttu-id="f6a76-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f6a76-140">System.Boolean</span></span>

## <span data-ttu-id="f6a76-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f6a76-141">NOTES</span></span>

## <span data-ttu-id="f6a76-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f6a76-142">RELATED LINKS</span></span>
