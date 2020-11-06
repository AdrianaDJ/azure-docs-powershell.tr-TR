---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
ms.openlocfilehash: d65e19cb86a2ba850311fa937e64432ee8588d02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593490"
---
# <span data-ttu-id="b4095-101">Get-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="b4095-101">Get-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="b4095-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4095-102">SYNOPSIS</span></span>
<span data-ttu-id="b4095-103">Bir olay hub ad alanının ayrıntılarını alır veya geçerli Azure aboneliğindeki tüm olay hub 'Larının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="b4095-103">Gets the details of an Event Hubs namespace, or gets a list of all Event Hubs namespaces in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4095-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b4095-104">SYNTAX</span></span>

```
Get-AzureRmEventHubNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4095-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b4095-105">DESCRIPTION</span></span>
<span data-ttu-id="b4095-106">Get-AzureRmEventHubNamespace cmdlet 'i, belirtilen bir olay hub ad alanının ayrıntılarını veya geçerli Azure aboneliğindeki tüm olay hub 'Larının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="b4095-106">The Get-AzureRmEventHubNamespace cmdlet gets either the details of a specified Event Hubs namespace, or a list of all Event Hubs namespaces in the current Azure subscription.</span></span>
<span data-ttu-id="b4095-107">Ad alanı adı sağlanmışsa, tek bir olay hub ad alanının ayrıntıları verilir.</span><span class="sxs-lookup"><span data-stu-id="b4095-107">If the namespace name is provided, the details of a single Event Hubs namespace is returned.</span></span>
<span data-ttu-id="b4095-108">Ad alanı adı sağlanmazsa, ad alanları listesi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="b4095-108">If the namespace name is not provided, a list of namespaces is returned.</span></span>

## <span data-ttu-id="b4095-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b4095-109">EXAMPLES</span></span>

### <span data-ttu-id="b4095-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b4095-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="b4095-111">\` \` Myresourcegroupname kaynak grubundaki cynamespacadındaki Olay Hub ad alanının ayrıntılarını alır \` \` .</span><span class="sxs-lookup"><span data-stu-id="b4095-111">Gets the details of the Event Hubs namespace \`MyNamespaceName\` in the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="b4095-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b4095-112">PARAMETERS</span></span>

### <span data-ttu-id="b4095-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4095-113">-DefaultProfile</span></span>
<span data-ttu-id="b4095-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b4095-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4095-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="b4095-115">-Name</span></span>
<span data-ttu-id="b4095-116">EventHub ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="b4095-116">EventHub Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4095-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4095-117">-ResourceGroupName</span></span>
<span data-ttu-id="b4095-118">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="b4095-118">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4095-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4095-119">CommonParameters</span></span>
<span data-ttu-id="b4095-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b4095-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b4095-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4095-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4095-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b4095-122">INPUTS</span></span>

### <span data-ttu-id="b4095-123">System. String</span><span class="sxs-lookup"><span data-stu-id="b4095-123">System.String</span></span>


## <span data-ttu-id="b4095-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b4095-124">OUTPUTS</span></span>

### <span data-ttu-id="b4095-125">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. EventHub. modeller. PSNamespaceAttributes, Microsoft. Azure. Commands. EventHub, Version = 0.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b4095-125">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes, Microsoft.Azure.Commands.EventHub, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="b4095-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b4095-126">NOTES</span></span>

## <span data-ttu-id="b4095-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b4095-127">RELATED LINKS</span></span>
