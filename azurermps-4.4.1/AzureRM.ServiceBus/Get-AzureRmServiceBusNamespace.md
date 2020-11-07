---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 2e6e044d888386b56d04ad48b7fbdaedadbd7497
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762194"
---
# <span data-ttu-id="ca9e7-101">Get-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="ca9e7-101">Get-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="ca9e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca9e7-102">SYNOPSIS</span></span>
<span data-ttu-id="ca9e7-103">Kaynak grubunda belirtilen Service Bus ad alanı için bir açıklama alır.</span><span class="sxs-lookup"><span data-stu-id="ca9e7-103">Gets a description for the specified Service Bus namespace within the resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca9e7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ca9e7-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusNamespace [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca9e7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ca9e7-105">DESCRIPTION</span></span>
<span data-ttu-id="ca9e7-106">**Get-AzureRmServiceBusNamespace** cmdlet 'i, kaynak grubunda belirtilen Service Bus ad alanı için bir açıklama alır.</span><span class="sxs-lookup"><span data-stu-id="ca9e7-106">The **Get-AzureRmServiceBusNamespace** cmdlet gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="ca9e7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ca9e7-107">EXAMPLES</span></span>

### <span data-ttu-id="ca9e7-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ca9e7-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="ca9e7-109">Belirtilen hizmet veri yolu ad alanının açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="ca9e7-109">Returns a description of the specified Service Bus namespace.</span></span>

## <span data-ttu-id="ca9e7-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ca9e7-110">PARAMETERS</span></span>

### <span data-ttu-id="ca9e7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca9e7-111">-DefaultProfile</span></span>
<span data-ttu-id="ca9e7-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ca9e7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca9e7-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="ca9e7-113">-Name</span></span>
<span data-ttu-id="ca9e7-114">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="ca9e7-114">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca9e7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca9e7-115">-ResourceGroupName</span></span>
<span data-ttu-id="ca9e7-116">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="ca9e7-116">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca9e7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca9e7-117">CommonParameters</span></span>
<span data-ttu-id="ca9e7-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ca9e7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca9e7-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca9e7-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca9e7-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ca9e7-120">INPUTS</span></span>

### <span data-ttu-id="ca9e7-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ca9e7-121">-ResourceGroup</span></span>
<span data-ttu-id="ca9e7-122">System. String</span><span class="sxs-lookup"><span data-stu-id="ca9e7-122">System.String</span></span>

### <span data-ttu-id="ca9e7-123">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="ca9e7-123">-NamespaceName</span></span>
 <span data-ttu-id="ca9e7-124">System. String</span><span class="sxs-lookup"><span data-stu-id="ca9e7-124">System.String</span></span>

## <span data-ttu-id="ca9e7-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ca9e7-125">OUTPUTS</span></span>

### <span data-ttu-id="ca9e7-126">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. ServiceBus. modeller. NamespaceAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ca9e7-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.NamespaceAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="ca9e7-127">Ad: SB-Example1 ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1 konumu: Batı ABD SKU: ad: Standart, kapasite: 1, katman: Standart ProvisioningState: başarılı https://SB-Example1.servicebus.windows.net:443/ durum 1/20/2017 1:40:24 1/20/2017 1:40:01:</span><span class="sxs-lookup"><span data-stu-id="ca9e7-127">Name               : SB-Example1 Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1 Location           : West US Sku                : Name : Standard , Capacity : 1 , Tier : Standard ProvisioningState  : Succeeded Status             : Active CreatedAt          : 1/20/2017 1:40:01 AM UpdatedAt          : 1/20/2017 1:40:24 AM ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/ Enabled            : True</span></span>

## <span data-ttu-id="ca9e7-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ca9e7-128">NOTES</span></span>
## <span data-ttu-id="ca9e7-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ca9e7-129">RELATED LINKS</span></span>

## <span data-ttu-id="ca9e7-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ca9e7-130">RELATED LINKS</span></span>

