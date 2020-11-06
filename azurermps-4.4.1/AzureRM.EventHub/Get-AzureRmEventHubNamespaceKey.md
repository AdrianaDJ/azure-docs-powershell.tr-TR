---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: e91b7edacc575ac98eb78ae44c88be4f6873f34c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594710"
---
# <span data-ttu-id="ff01d-101">Get-AzureRmEventHubNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="ff01d-101">Get-AzureRmEventHubNamespaceKey</span></span>

## <span data-ttu-id="ff01d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff01d-102">SYNOPSIS</span></span>
<span data-ttu-id="ff01d-103">Belirtilen olay hub ad alanı yetkilendirme kuralındaki yetkilendirme kuralı için birincil, Ikincil ConnectionString ve Keys ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="ff01d-103">Gets details of Primary, Secondary connectionstrings and keys for the authorization rule of the specified Event Hubs namespace authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff01d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ff01d-104">SYNTAX</span></span>

```
Get-AzureRmEventHubNamespaceKey [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthorizationRuleName] <String>
```

## <span data-ttu-id="ff01d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ff01d-105">DESCRIPTION</span></span>
<span data-ttu-id="ff01d-106">Get-AzureRmEventHubNamespaceKey cmdlet 'i, verilen olay hub alanında belirtilen yetkilendirme kuralının birincil ve Ikincil ConnectionString ve anahtar ayrıntılarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="ff01d-106">The Get-AzureRmEventHubNamespaceKey cmdlet returns the Primary and Secondary connectionstrings and keys details of the specified authorization rule in the given Event Hubs namespace.</span></span>

## <span data-ttu-id="ff01d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ff01d-107">EXAMPLES</span></span>

### <span data-ttu-id="ff01d-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ff01d-108">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubNamespaceKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="ff01d-109">Birincil, Ikincil ConnectionString ve anahtarların, \` \` \` \` \` Myresourcegroupname kaynak grubunda yer alan Olay Hub 'ları ad alanı olan \` http</span><span class="sxs-lookup"><span data-stu-id="ff01d-109">Gets details of Primary, Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\` on the Event Hubs namespace \`MyNamespaceName\` in the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="ff01d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ff01d-110">PARAMETERS</span></span>

### <span data-ttu-id="ff01d-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="ff01d-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="ff01d-112">Olay Hub 'Ları ad alanında yetkilendirme kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="ff01d-112">The name of the authorization rule on the Event Hubs namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff01d-113">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="ff01d-113">-NamespaceName</span></span>
<span data-ttu-id="ff01d-114">Olay Hub 'Ları ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="ff01d-114">The Event Hubs namespace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff01d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff01d-115">-ResourceGroupName</span></span>
<span data-ttu-id="ff01d-116">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ff01d-116">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="ff01d-117">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ff01d-117">INPUTS</span></span>

### <span data-ttu-id="ff01d-118">System. String</span><span class="sxs-lookup"><span data-stu-id="ff01d-118">System.String</span></span>

## <span data-ttu-id="ff01d-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ff01d-119">OUTPUTS</span></span>

### <span data-ttu-id="ff01d-120">Microsoft. Azure. Commands. EventHub. modeller. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="ff01d-120">Microsoft.Azure.Commands.EventHub.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="ff01d-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ff01d-121">NOTES</span></span>

## <span data-ttu-id="ff01d-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ff01d-122">RELATED LINKS</span></span>

