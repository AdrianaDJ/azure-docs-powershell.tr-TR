---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 26a2e414f05fc0aeb209afa946ae168c59ea4ff8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937728"
---
# <span data-ttu-id="f98c5-101">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="f98c5-101">Get-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="f98c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f98c5-102">SYNOPSIS</span></span>
<span data-ttu-id="f98c5-103">Tümleştirme hesabı toplu iş yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="f98c5-103">Gets an integration account batch configuration.</span></span>

## <span data-ttu-id="f98c5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f98c5-104">SYNTAX</span></span>

### <span data-ttu-id="f98c5-105">Byıntegrationaccount (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f98c5-105">ByIntegrationAccount (Default)</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f98c5-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f98c5-106">ByInputObject</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f98c5-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="f98c5-107">ByResourceId</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f98c5-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f98c5-108">DESCRIPTION</span></span>
<span data-ttu-id="f98c5-109">**Get-Azıntegrationaccountbatchconfiguration** cmdlet 'i bir tümleştirme hesabından toplu iş yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="f98c5-109">The **Get-AzIntegrationAccountBatchConfiguration** cmdlet gets an batch configuration from an integration account.</span></span>

## <span data-ttu-id="f98c5-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f98c5-110">EXAMPLES</span></span>

### <span data-ttu-id="f98c5-111">Örnek 1: parametrelere göre toplu yapılandırma alma</span><span class="sxs-lookup"><span data-stu-id="f98c5-111">Example 1: Get a batch configuration by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="f98c5-112">"SampleResourceGroup" kaynak grubunda bulunan "Sampleıntegrationaccount" tümleştirme hesabında bulunan "sampleBatchConfig" adlı bir toplu iş yapılandırması alın.</span><span class="sxs-lookup"><span data-stu-id="f98c5-112">Get a batch configuration named "sampleBatchConfig" located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

### <span data-ttu-id="f98c5-113">Örnek 2: bir tümleştirme hesabındaki tüm toplu iş yapılandırmalarını parametrelere göre listeleme</span><span class="sxs-lookup"><span data-stu-id="f98c5-113">Example 2: List all batch configurations in an integration account by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig2
Name       : sampleBatchConfig2
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="f98c5-114">"SampleResourceGroup" kaynak grubunda bulunan "Sampleıntegrationaccount" tümleştirme hesabındaki tüm toplu iş yapılandırmalarını edinin.</span><span class="sxs-lookup"><span data-stu-id="f98c5-114">Get all batch configurations located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

## <span data-ttu-id="f98c5-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f98c5-115">PARAMETERS</span></span>

### <span data-ttu-id="f98c5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f98c5-116">-DefaultProfile</span></span>
<span data-ttu-id="f98c5-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f98c5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f98c5-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="f98c5-118">-Name</span></span>
<span data-ttu-id="f98c5-119">Tümleştirme hesabı toplu işlem yapılandırma adı.</span><span class="sxs-lookup"><span data-stu-id="f98c5-119">The integration account batch configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BatchConfigurationName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f98c5-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="f98c5-120">-ParentName</span></span>
<span data-ttu-id="f98c5-121">Tümleştirme hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="f98c5-121">The integration account name.</span></span>

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

### <span data-ttu-id="f98c5-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f98c5-122">-ParentObject</span></span>
<span data-ttu-id="f98c5-123">Tümleştirme hesabı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="f98c5-123">An integration account object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Logic.Models.IntegrationAccount
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f98c5-124">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="f98c5-124">-ParentResourceId</span></span>
<span data-ttu-id="f98c5-125">Tümleştirme hesabı kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="f98c5-125">The integration account resource id.</span></span>

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

### <span data-ttu-id="f98c5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f98c5-126">-ResourceGroupName</span></span>
<span data-ttu-id="f98c5-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f98c5-127">The resource group name.</span></span>

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

### <span data-ttu-id="f98c5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f98c5-128">CommonParameters</span></span>
<span data-ttu-id="f98c5-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f98c5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f98c5-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f98c5-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f98c5-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f98c5-131">INPUTS</span></span>

### <span data-ttu-id="f98c5-132">Microsoft. Azure. Management. Logic. modeller. ıntegrationhesabı</span><span class="sxs-lookup"><span data-stu-id="f98c5-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="f98c5-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f98c5-133">System.String</span></span>

## <span data-ttu-id="f98c5-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f98c5-134">OUTPUTS</span></span>

### <span data-ttu-id="f98c5-135">Microsoft. Azure. Commands. Logicuyg. modeller. Psıntegrationaccountbatchconfiguration</span><span class="sxs-lookup"><span data-stu-id="f98c5-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="f98c5-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f98c5-136">NOTES</span></span>

## <span data-ttu-id="f98c5-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f98c5-137">RELATED LINKS</span></span>
