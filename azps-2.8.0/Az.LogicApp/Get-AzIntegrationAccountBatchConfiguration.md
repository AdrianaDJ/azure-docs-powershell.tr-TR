---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 5920ba51d4b067b7c47de6c471240a193efb3e5f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751567"
---
# <span data-ttu-id="9843f-101">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="9843f-101">Get-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="9843f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9843f-102">SYNOPSIS</span></span>
<span data-ttu-id="9843f-103">Tümleştirme hesabı toplu iş yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="9843f-103">Gets an integration account batch configuration.</span></span>

## <span data-ttu-id="9843f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9843f-104">SYNTAX</span></span>

### <span data-ttu-id="9843f-105">Byıntegrationaccount (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9843f-105">ByIntegrationAccount (Default)</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9843f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9843f-106">ByInputObject</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9843f-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="9843f-107">ByResourceId</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9843f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9843f-108">DESCRIPTION</span></span>
<span data-ttu-id="9843f-109">**Get-Azıntegrationaccountbatchconfiguration** cmdlet 'i bir tümleştirme hesabından toplu iş yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="9843f-109">The **Get-AzIntegrationAccountBatchConfiguration** cmdlet gets an batch configuration from an integration account.</span></span>

## <span data-ttu-id="9843f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9843f-110">EXAMPLES</span></span>

### <span data-ttu-id="9843f-111">Örnek 1: parametrelere göre toplu yapılandırma alma</span><span class="sxs-lookup"><span data-stu-id="9843f-111">Example 1: Get a batch configuration by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="9843f-112">"SampleResourceGroup" kaynak grubunda bulunan "Sampleıntegrationaccount" tümleştirme hesabında bulunan "sampleBatchConfig" adlı bir toplu iş yapılandırması alın.</span><span class="sxs-lookup"><span data-stu-id="9843f-112">Get a batch configuration named "sampleBatchConfig" located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

### <span data-ttu-id="9843f-113">Örnek 2: bir tümleştirme hesabındaki tüm toplu iş yapılandırmalarını parametrelere göre listeleme</span><span class="sxs-lookup"><span data-stu-id="9843f-113">Example 2: List all batch configurations in an integration account by parameters</span></span>
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

<span data-ttu-id="9843f-114">"SampleResourceGroup" kaynak grubunda bulunan "Sampleıntegrationaccount" tümleştirme hesabındaki tüm toplu iş yapılandırmalarını edinin.</span><span class="sxs-lookup"><span data-stu-id="9843f-114">Get all batch configurations located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

## <span data-ttu-id="9843f-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9843f-115">PARAMETERS</span></span>

### <span data-ttu-id="9843f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9843f-116">-DefaultProfile</span></span>
<span data-ttu-id="9843f-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9843f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9843f-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="9843f-118">-Name</span></span>
<span data-ttu-id="9843f-119">Tümleştirme hesabı toplu işlem yapılandırma adı.</span><span class="sxs-lookup"><span data-stu-id="9843f-119">The integration account batch configuration name.</span></span>

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

### <span data-ttu-id="9843f-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="9843f-120">-ParentName</span></span>
<span data-ttu-id="9843f-121">Tümleştirme hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="9843f-121">The integration account name.</span></span>

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

### <span data-ttu-id="9843f-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9843f-122">-ParentObject</span></span>
<span data-ttu-id="9843f-123">Tümleştirme hesabı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="9843f-123">An integration account object.</span></span>

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

### <span data-ttu-id="9843f-124">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="9843f-124">-ParentResourceId</span></span>
<span data-ttu-id="9843f-125">Tümleştirme hesabı kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="9843f-125">The integration account resource id.</span></span>

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

### <span data-ttu-id="9843f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9843f-126">-ResourceGroupName</span></span>
<span data-ttu-id="9843f-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="9843f-127">The resource group name.</span></span>

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

### <span data-ttu-id="9843f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9843f-128">CommonParameters</span></span>
<span data-ttu-id="9843f-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9843f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9843f-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9843f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9843f-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9843f-131">INPUTS</span></span>

### <span data-ttu-id="9843f-132">Microsoft. Azure. Management. Logic. modeller. ıntegrationhesabı</span><span class="sxs-lookup"><span data-stu-id="9843f-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="9843f-133">System. String</span><span class="sxs-lookup"><span data-stu-id="9843f-133">System.String</span></span>

## <span data-ttu-id="9843f-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9843f-134">OUTPUTS</span></span>

### <span data-ttu-id="9843f-135">Microsoft. Azure. Commands. Logicuyg. modeller. Psıntegrationaccountbatchconfiguration</span><span class="sxs-lookup"><span data-stu-id="9843f-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="9843f-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9843f-136">NOTES</span></span>

## <span data-ttu-id="9843f-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9843f-137">RELATED LINKS</span></span>
