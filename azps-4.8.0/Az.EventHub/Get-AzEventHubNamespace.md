---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNamespace.md
ms.openlocfilehash: ba2209f7b58951bdc52976fb3cbab10fa15da98a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108287"
---
# <span data-ttu-id="91184-101">Get-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="91184-101">Get-AzEventHubNamespace</span></span>

## <span data-ttu-id="91184-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91184-102">SYNOPSIS</span></span>
<span data-ttu-id="91184-103">Bir olay hub ad alanının ayrıntılarını alır veya geçerli Azure aboneliğindeki tüm olay hub 'Larının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="91184-103">Gets the details of an Event Hubs namespace, or gets a list of all Event Hubs namespaces in the current Azure subscription.</span></span>

## <span data-ttu-id="91184-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="91184-104">SYNTAX</span></span>

```
Get-AzEventHubNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91184-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="91184-105">DESCRIPTION</span></span>
<span data-ttu-id="91184-106">Get-AzEventHubNamespace cmdlet 'i, belirtilen bir olay hub ad alanının ayrıntılarını veya geçerli Azure aboneliğindeki tüm olay hub 'Larının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="91184-106">The Get-AzEventHubNamespace cmdlet gets either the details of a specified Event Hubs namespace, or a list of all Event Hubs namespaces in the current Azure subscription.</span></span>
<span data-ttu-id="91184-107">Ad alanı adı sağlanmışsa, tek bir olay hub ad alanının ayrıntıları verilir.</span><span class="sxs-lookup"><span data-stu-id="91184-107">If the namespace name is provided, the details of a single Event Hubs namespace is returned.</span></span>
<span data-ttu-id="91184-108">Ad alanı adı sağlanmazsa, ad alanları listesi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="91184-108">If the namespace name is not provided, a list of namespaces is returned.</span></span>

## <span data-ttu-id="91184-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="91184-109">EXAMPLES</span></span>

### <span data-ttu-id="91184-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="91184-110">Example 1</span></span>
```
PS C:\> Get-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   :
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
KafkaEnabled           : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10
```

<span data-ttu-id="91184-111">\` \` Myresourcegroupname kaynak grubundaki mynamespacename öğesinin ayrıntılarını alır \` \` .</span><span class="sxs-lookup"><span data-stu-id="91184-111">Gets the details of namespace \`MyNamespaceName\` in the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="91184-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="91184-112">PARAMETERS</span></span>

### <span data-ttu-id="91184-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91184-113">-DefaultProfile</span></span>
<span data-ttu-id="91184-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="91184-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91184-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="91184-115">-Name</span></span>
<span data-ttu-id="91184-116">EventHub ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="91184-116">EventHub Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91184-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91184-117">-ResourceGroupName</span></span>
<span data-ttu-id="91184-118">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="91184-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91184-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91184-119">CommonParameters</span></span>
<span data-ttu-id="91184-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="91184-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91184-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91184-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91184-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="91184-122">INPUTS</span></span>

### <span data-ttu-id="91184-123">System. String</span><span class="sxs-lookup"><span data-stu-id="91184-123">System.String</span></span>

## <span data-ttu-id="91184-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="91184-124">OUTPUTS</span></span>

### <span data-ttu-id="91184-125">Microsoft. Azure. Commands. EventHub. model. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="91184-125">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="91184-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="91184-126">NOTES</span></span>

## <span data-ttu-id="91184-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="91184-127">RELATED LINKS</span></span>
