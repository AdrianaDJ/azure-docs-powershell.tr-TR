---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 64dae906f7f28e119d8550ecf5bb31d1b6ca7b27
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935893"
---
# <span data-ttu-id="386ac-101">Get-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="386ac-101">Get-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="386ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="386ac-102">SYNOPSIS</span></span>
<span data-ttu-id="386ac-103">Geçerli Azure aboneliğindeki bir olay hub ağ kuralı ad alanının ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="386ac-103">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="386ac-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="386ac-104">SYNTAX</span></span>

### <span data-ttu-id="386ac-105">NetworkRuleSetPropertiesSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="386ac-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="386ac-106">NetworkRuleSetNamespacePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="386ac-106">NetworkRuleSetNamespacePropertiesSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="386ac-107">Networkrulesetresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="386ac-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="386ac-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="386ac-108">DESCRIPTION</span></span>
<span data-ttu-id="386ac-109">Geçerli Azure aboneliğindeki bir olay hub ağ kuralı ad alanının ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="386ac-109">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="386ac-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="386ac-110">EXAMPLES</span></span>

### <span data-ttu-id="386ac-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="386ac-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375
```

<span data-ttu-id="386ac-112">ResourceGroup ve Namespace parametrelerini kullanarak, Olay Hub 'Larının ağ kural kümesi ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="386ac-112">Get the details of Event Hubs NetworkruleSet of namespace using ResourceGroup and Namespace parameters.</span></span> 

### <span data-ttu-id="386ac-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="386ac-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -Namespace Eventhub-Namespace1-2389
```

<span data-ttu-id="386ac-114">Geçerli abonelikteki ad alanı kullanarak, Olay Hub 'Ları olan ad alanının ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="386ac-114">Get the details of Event Hubs NetworkruleSet of namespace using  Namespace which is in the current subscription.</span></span>

### <span data-ttu-id="386ac-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="386ac-115">Example 3</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-2389
```

<span data-ttu-id="386ac-116">Diğer ad alanının kaynak kimliğini kullanarak, Olay Hub 'Larının ağ kuralı ad kümesinin ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="386ac-116">Get the details of Event Hubs NetworkruleSet of namespace using Resource Id of other Namespace</span></span> 

## <span data-ttu-id="386ac-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="386ac-117">PARAMETERS</span></span>

### <span data-ttu-id="386ac-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="386ac-118">-DefaultProfile</span></span>
<span data-ttu-id="386ac-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="386ac-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="386ac-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="386ac-120">-Namespace</span></span>
<span data-ttu-id="386ac-121">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="386ac-121">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet, NetworkRuleSetNamespacePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="386ac-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="386ac-122">-ResourceGroupName</span></span>
<span data-ttu-id="386ac-123">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="386ac-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetNamespacePropertiesSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="386ac-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="386ac-124">-ResourceId</span></span>
<span data-ttu-id="386ac-125">Ad alanı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="386ac-125">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="386ac-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="386ac-126">CommonParameters</span></span>
<span data-ttu-id="386ac-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="386ac-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="386ac-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="386ac-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="386ac-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="386ac-129">INPUTS</span></span>

### <span data-ttu-id="386ac-130">System. String</span><span class="sxs-lookup"><span data-stu-id="386ac-130">System.String</span></span>

## <span data-ttu-id="386ac-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="386ac-131">OUTPUTS</span></span>

### <span data-ttu-id="386ac-132">Microsoft. Azure. Commands. EventHub. model. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="386ac-132">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="386ac-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="386ac-133">NOTES</span></span>

## <span data-ttu-id="386ac-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="386ac-134">RELATED LINKS</span></span>