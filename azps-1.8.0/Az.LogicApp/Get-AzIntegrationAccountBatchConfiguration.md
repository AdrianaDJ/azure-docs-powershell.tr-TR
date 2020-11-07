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
ms.locfileid: "93916112"
---
# <span data-ttu-id="9cd25-101">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="9cd25-101">Get-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="9cd25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cd25-102">SYNOPSIS</span></span>
<span data-ttu-id="9cd25-103">Tümleştirme hesabı toplu iş yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="9cd25-103">Gets an integration account batch configuration.</span></span>

## <span data-ttu-id="9cd25-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9cd25-104">SYNTAX</span></span>

### <span data-ttu-id="9cd25-105">Byıntegrationaccount (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9cd25-105">ByIntegrationAccount (Default)</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9cd25-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9cd25-106">ByInputObject</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9cd25-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="9cd25-107">ByResourceId</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9cd25-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9cd25-108">DESCRIPTION</span></span>
<span data-ttu-id="9cd25-109">**Get-Azıntegrationaccountbatchconfiguration** cmdlet 'i bir tümleştirme hesabından toplu iş yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="9cd25-109">The **Get-AzIntegrationAccountBatchConfiguration** cmdlet gets an batch configuration from an integration account.</span></span>

## <span data-ttu-id="9cd25-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9cd25-110">EXAMPLES</span></span>

### <span data-ttu-id="9cd25-111">Örnek 1: parametrelere göre toplu yapılandırma alma</span><span class="sxs-lookup"><span data-stu-id="9cd25-111">Example 1: Get a batch configuration by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="9cd25-112">"SampleResourceGroup" kaynak grubunda bulunan "Sampleıntegrationaccount" tümleştirme hesabında bulunan "sampleBatchConfig" adlı bir toplu iş yapılandırması alın.</span><span class="sxs-lookup"><span data-stu-id="9cd25-112">Get a batch configuration named "sampleBatchConfig" located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

### <span data-ttu-id="9cd25-113">Örnek 2: bir tümleştirme hesabındaki tüm toplu iş yapılandırmalarını parametrelere göre listeleme</span><span class="sxs-lookup"><span data-stu-id="9cd25-113">Example 2: List all batch configurations in an integration account by parameters</span></span>
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

<span data-ttu-id="9cd25-114">"SampleResourceGroup" kaynak grubunda bulunan "Sampleıntegrationaccount" tümleştirme hesabındaki tüm toplu iş yapılandırmalarını edinin.</span><span class="sxs-lookup"><span data-stu-id="9cd25-114">Get all batch configurations located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

## <span data-ttu-id="9cd25-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9cd25-115">PARAMETERS</span></span>

### <span data-ttu-id="9cd25-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cd25-116">-DefaultProfile</span></span>
<span data-ttu-id="9cd25-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9cd25-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cd25-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="9cd25-118">-Name</span></span>
<span data-ttu-id="9cd25-119">Tümleştirme hesabı toplu işlem yapılandırma adı.</span><span class="sxs-lookup"><span data-stu-id="9cd25-119">The integration account batch configuration name.</span></span>

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

### <span data-ttu-id="9cd25-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="9cd25-120">-ParentName</span></span>
<span data-ttu-id="9cd25-121">Tümleştirme hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="9cd25-121">The integration account name.</span></span>

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

### <span data-ttu-id="9cd25-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9cd25-122">-ParentObject</span></span>
<span data-ttu-id="9cd25-123">Tümleştirme hesabı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="9cd25-123">An integration account object.</span></span>

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

### <span data-ttu-id="9cd25-124">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="9cd25-124">-ParentResourceId</span></span>
<span data-ttu-id="9cd25-125">Tümleştirme hesabı kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="9cd25-125">The integration account resource id.</span></span>

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

### <span data-ttu-id="9cd25-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cd25-126">-ResourceGroupName</span></span>
<span data-ttu-id="9cd25-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="9cd25-127">The resource group name.</span></span>

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

### <span data-ttu-id="9cd25-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cd25-128">CommonParameters</span></span>
<span data-ttu-id="9cd25-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9cd25-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cd25-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cd25-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cd25-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9cd25-131">INPUTS</span></span>

### <span data-ttu-id="9cd25-132">Microsoft. Azure. Management. Logic. modeller. ıntegrationhesabı</span><span class="sxs-lookup"><span data-stu-id="9cd25-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="9cd25-133">System. String</span><span class="sxs-lookup"><span data-stu-id="9cd25-133">System.String</span></span>

## <span data-ttu-id="9cd25-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9cd25-134">OUTPUTS</span></span>

### <span data-ttu-id="9cd25-135">Microsoft. Azure. Commands. Logicuyg. modeller. Psıntegrationaccountbatchconfiguration</span><span class="sxs-lookup"><span data-stu-id="9cd25-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="9cd25-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9cd25-136">NOTES</span></span>

## <span data-ttu-id="9cd25-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9cd25-137">RELATED LINKS</span></span>