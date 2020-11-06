---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 1834adfdb275bc5454e16e72732b649c82704a34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591613"
---
# <span data-ttu-id="ea50e-101">New-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="ea50e-101">New-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="ea50e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea50e-102">SYNOPSIS</span></span>
<span data-ttu-id="ea50e-103">Yeni bir hizmet veri yolu ad alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ea50e-103">Creates a new Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea50e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ea50e-104">SYNTAX</span></span>

```
New-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-SkuName <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ea50e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ea50e-105">DESCRIPTION</span></span>
<span data-ttu-id="ea50e-106">**Yeni-AzureRmServiceBusNamespace** cmdlet 'i yeni bir hizmet veri yolu ad alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ea50e-106">The **New-AzureRmServiceBusNamespace** cmdlet creates a new Service Bus namespace.</span></span> <span data-ttu-id="ea50e-107">Oluşturulduktan sonra, ad alanı kaynak bildirimi sabittir.</span><span class="sxs-lookup"><span data-stu-id="ea50e-107">Once created, the namespace resource manifest is immutable.</span></span> <span data-ttu-id="ea50e-108">Bu işlem idempotent.</span><span class="sxs-lookup"><span data-stu-id="ea50e-108">This operation is idempotent.</span></span>

## <span data-ttu-id="ea50e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ea50e-109">EXAMPLES</span></span>

### <span data-ttu-id="ea50e-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ea50e-110">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -Location WestUS -SkuName "Standard" -Tag @{Tag1="Tag1Value"}

Name               : SB-Example1
Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
Location           : West US
Sku                : Name : Standard , Capacity : 1 , Tier : Standard
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 2:07:33 AM
UpdatedAt          : 1/20/2017 2:07:56 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
```

<span data-ttu-id="ea50e-111">Belirtilen kaynak grubunda yeni bir hizmet veri yolu ad alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ea50e-111">Creates a new Service Bus namespace within the specified resource group.</span></span>

## <span data-ttu-id="ea50e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ea50e-112">PARAMETERS</span></span>

### <span data-ttu-id="ea50e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea50e-113">-DefaultProfile</span></span>
<span data-ttu-id="ea50e-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ea50e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea50e-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="ea50e-115">-Location</span></span>
<span data-ttu-id="ea50e-116">Hizmet veri yolu ad alanı konumu.</span><span class="sxs-lookup"><span data-stu-id="ea50e-116">The Service Bus namespace location.</span></span>

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

### <span data-ttu-id="ea50e-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="ea50e-117">-Name</span></span>
<span data-ttu-id="ea50e-118">ServiceBus ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="ea50e-118">ServiceBus Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea50e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea50e-119">-ResourceGroupName</span></span>
<span data-ttu-id="ea50e-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ea50e-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea50e-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ea50e-121">-SkuName</span></span>
<span data-ttu-id="ea50e-122">Hizmet veri yolu ad alanı SKU adı.</span><span class="sxs-lookup"><span data-stu-id="ea50e-122">The Service Bus namespace SKU name.</span></span>

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

### <span data-ttu-id="ea50e-123">Etiketli</span><span class="sxs-lookup"><span data-stu-id="ea50e-123">-Tag</span></span>
<span data-ttu-id="ea50e-124">Sunucuda etiket olarak ayarlanan karma tablo biçimindeki anahtar değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="ea50e-124">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="ea50e-125">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="ea50e-125">For example:</span></span>

<span data-ttu-id="ea50e-126">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="ea50e-126">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ea50e-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="ea50e-127">-Confirm</span></span>
<span data-ttu-id="ea50e-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ea50e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea50e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea50e-129">-WhatIf</span></span>
<span data-ttu-id="ea50e-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ea50e-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea50e-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ea50e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea50e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea50e-132">CommonParameters</span></span>
<span data-ttu-id="ea50e-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ea50e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea50e-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea50e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea50e-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ea50e-135">INPUTS</span></span>

### <span data-ttu-id="ea50e-136">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ea50e-136">-ResourceGroup</span></span>
 <span data-ttu-id="ea50e-137">System. String</span><span class="sxs-lookup"><span data-stu-id="ea50e-137">System.String</span></span>

### <span data-ttu-id="ea50e-138">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="ea50e-138">-NamespaceName</span></span>
 <span data-ttu-id="ea50e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ea50e-139">System.String</span></span>

### <span data-ttu-id="ea50e-140">-Konum</span><span class="sxs-lookup"><span data-stu-id="ea50e-140">-Location</span></span>
 <span data-ttu-id="ea50e-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ea50e-141">System.String</span></span>

### <span data-ttu-id="ea50e-142">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ea50e-142">-SkuName</span></span>
 <span data-ttu-id="ea50e-143">System. String</span><span class="sxs-lookup"><span data-stu-id="ea50e-143">System.String</span></span>

### <span data-ttu-id="ea50e-144">Etiketli</span><span class="sxs-lookup"><span data-stu-id="ea50e-144">-Tag</span></span>
 <span data-ttu-id="ea50e-145">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ea50e-145">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ea50e-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ea50e-146">OUTPUTS</span></span>

### <span data-ttu-id="ea50e-147">Microsoft. Azure. Commands. ServiceBus. modeller. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="ea50e-147">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="ea50e-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ea50e-148">NOTES</span></span>

## <span data-ttu-id="ea50e-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ea50e-149">RELATED LINKS</span></span>

