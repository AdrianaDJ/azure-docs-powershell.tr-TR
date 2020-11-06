---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 79b55b62c3f4add24e52a36756f83bd16466edbd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593799"
---
# <span data-ttu-id="1eb79-101">New-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="1eb79-101">New-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="1eb79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1eb79-102">SYNOPSIS</span></span>
<span data-ttu-id="1eb79-103">Yeni bir hizmet veri yolu ad alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1eb79-103">Creates a new Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1eb79-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1eb79-104">SYNTAX</span></span>

```
New-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-NamespaceName] <String>
 [-SkuName <String>] [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1eb79-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1eb79-105">DESCRIPTION</span></span>
<span data-ttu-id="1eb79-106">**Yeni-AzureRmServiceBusNamespace** cmdlet 'i yeni bir hizmet veri yolu ad alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1eb79-106">The **New-AzureRmServiceBusNamespace** cmdlet creates a new Service Bus namespace.</span></span> <span data-ttu-id="1eb79-107">Oluşturulduktan sonra, ad alanı kaynak bildirimi sabittir.</span><span class="sxs-lookup"><span data-stu-id="1eb79-107">Once created, the namespace resource manifest is immutable.</span></span> <span data-ttu-id="1eb79-108">Bu işlem idempotent.</span><span class="sxs-lookup"><span data-stu-id="1eb79-108">This operation is idempotent.</span></span>

## <span data-ttu-id="1eb79-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1eb79-109">EXAMPLES</span></span>

### <span data-ttu-id="1eb79-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1eb79-110">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUS -SkuName "Standard" -Tag @{Tag1="Tag1Value"}

Name               : SB-Example1
Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
Location           : West US
Sku                : Name : Standard , Capacity : 1 , Tier : Standard
ProvisioningState  : Succeeded
Status             : Active
CreatedAt          : 1/20/2017 2:07:33 AM
UpdatedAt          : 1/20/2017 2:07:56 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
Enabled            : True
```

<span data-ttu-id="1eb79-111">Belirtilen kaynak grubunda yeni bir hizmet veri yolu ad alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1eb79-111">Creates a new Service Bus namespace within the specified resource group.</span></span>

## <span data-ttu-id="1eb79-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1eb79-112">PARAMETERS</span></span>

### <span data-ttu-id="1eb79-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="1eb79-113">-Location</span></span>
<span data-ttu-id="1eb79-114">Hizmet veri yolu ad alanı konumu.</span><span class="sxs-lookup"><span data-stu-id="1eb79-114">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="1eb79-115">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="1eb79-115">-NamespaceName</span></span>
<span data-ttu-id="1eb79-116">Hizmet veri yolu ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="1eb79-116">The Service Bus namespace name.</span></span>

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

### <span data-ttu-id="1eb79-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1eb79-117">-ResourceGroupName</span></span>
<span data-ttu-id="1eb79-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="1eb79-118">The resource group name.</span></span>

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

### <span data-ttu-id="1eb79-119">-SkuName</span><span class="sxs-lookup"><span data-stu-id="1eb79-119">-SkuName</span></span>
<span data-ttu-id="1eb79-120">Hizmet veri yolu ad alanı SKU adı.</span><span class="sxs-lookup"><span data-stu-id="1eb79-120">The Service Bus namespace SKU name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1eb79-121">Etiketli</span><span class="sxs-lookup"><span data-stu-id="1eb79-121">-Tag</span></span>
<span data-ttu-id="1eb79-122">Sunucuda etiket olarak ayarlanan karma tablo biçimindeki anahtar değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="1eb79-122">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="1eb79-123">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="1eb79-123">For example:</span></span>

<span data-ttu-id="1eb79-124">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="1eb79-124">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1eb79-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="1eb79-125">-Confirm</span></span>
<span data-ttu-id="1eb79-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1eb79-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eb79-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1eb79-127">-WhatIf</span></span>
<span data-ttu-id="1eb79-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1eb79-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1eb79-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1eb79-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eb79-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1eb79-130">CommonParameters</span></span>
<span data-ttu-id="1eb79-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1eb79-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1eb79-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1eb79-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1eb79-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1eb79-133">INPUTS</span></span>

### <span data-ttu-id="1eb79-134">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1eb79-134">-ResourceGroup</span></span>
 <span data-ttu-id="1eb79-135">System. String</span><span class="sxs-lookup"><span data-stu-id="1eb79-135">System.String</span></span>

### <span data-ttu-id="1eb79-136">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="1eb79-136">-NamespaceName</span></span>
 <span data-ttu-id="1eb79-137">System. String</span><span class="sxs-lookup"><span data-stu-id="1eb79-137">System.String</span></span>

### <span data-ttu-id="1eb79-138">-Konum</span><span class="sxs-lookup"><span data-stu-id="1eb79-138">-Location</span></span>
 <span data-ttu-id="1eb79-139">System. String</span><span class="sxs-lookup"><span data-stu-id="1eb79-139">System.String</span></span>

### <span data-ttu-id="1eb79-140">-SkuName</span><span class="sxs-lookup"><span data-stu-id="1eb79-140">-SkuName</span></span>
 <span data-ttu-id="1eb79-141">System. String</span><span class="sxs-lookup"><span data-stu-id="1eb79-141">System.String</span></span>

### <span data-ttu-id="1eb79-142">Etiketli</span><span class="sxs-lookup"><span data-stu-id="1eb79-142">-Tag</span></span>
 <span data-ttu-id="1eb79-143">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1eb79-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1eb79-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1eb79-144">OUTPUTS</span></span>

### <span data-ttu-id="1eb79-145">Microsoft. Azure. Commands. ServiceBus. modeller. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="1eb79-145">Microsoft.Azure.Commands.ServiceBus.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="1eb79-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1eb79-146">NOTES</span></span>

## <span data-ttu-id="1eb79-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1eb79-147">RELATED LINKS</span></span>
