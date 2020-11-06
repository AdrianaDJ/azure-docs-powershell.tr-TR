---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/new-azurermrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayNamespace.md
ms.openlocfilehash: 1eed6f722487e3c37d9d12785b07e90516406f8f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591637"
---
# <span data-ttu-id="7f993-101">New-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="7f993-101">New-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="7f993-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f993-102">SYNOPSIS</span></span>
<span data-ttu-id="7f993-103">Yeni bir geçiş ad alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7f993-103">Creates a new Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f993-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7f993-104">SYNTAX</span></span>

```
New-AzureRmRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f993-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7f993-105">DESCRIPTION</span></span>
<span data-ttu-id="7f993-106">**New-AzureRmRelayNamespace** cmdlet 'i yeni bir geçiş ad alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7f993-106">The **New-AzureRmRelayNamespace** cmdlet creates a new Relay namespace.</span></span> <span data-ttu-id="7f993-107">Oluşturulduktan sonra, ad alanı kaynak bildirimi sabittir.</span><span class="sxs-lookup"><span data-stu-id="7f993-107">Once created, the namespace resource manifest is immutable.</span></span>

## <span data-ttu-id="7f993-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7f993-108">EXAMPLES</span></span>

### <span data-ttu-id="7f993-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7f993-109">Example 1</span></span>
```
PS C:\> New-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Location "West US" -Tag @{Tag1="Tag1Value"}

ProvisioningState  : Succeeded
CreatedAt          : 4/12/2017 12:38:47 AM
UpdatedAt          : 4/12/2017 12:39:10 AM
ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/
MetricId           : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX:testnamespace-relay1
Location           : West US
Tags               : {[tag1, Tag1Value]}
Id                 : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1
Name               : TestNameSpace-Relay1
Type               : Microsoft.Relay/namespaces
```

<span data-ttu-id="7f993-110">Belirtilen kaynak grubunda yeni bir geçiş ad alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7f993-110">Creates a new Relay namespace within the specified resource group.</span></span>

## <span data-ttu-id="7f993-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7f993-111">PARAMETERS</span></span>

### <span data-ttu-id="7f993-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f993-112">-DefaultProfile</span></span>
<span data-ttu-id="7f993-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7f993-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f993-114">-Konum</span><span class="sxs-lookup"><span data-stu-id="7f993-114">-Location</span></span>
<span data-ttu-id="7f993-115">Geçiş ad alanı konumu.</span><span class="sxs-lookup"><span data-stu-id="7f993-115">Relay Namespace Location.</span></span>

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

### <span data-ttu-id="7f993-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="7f993-116">-Name</span></span>
<span data-ttu-id="7f993-117">Geçiş ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="7f993-117">Relay Namespace Name</span></span>

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

### <span data-ttu-id="7f993-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f993-118">-ResourceGroupName</span></span>
<span data-ttu-id="7f993-119">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="7f993-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="7f993-120">Etiketli</span><span class="sxs-lookup"><span data-stu-id="7f993-120">-Tag</span></span>
<span data-ttu-id="7f993-121">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="7f993-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7f993-122">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="7f993-122">For example:</span></span>

<span data-ttu-id="7f993-123">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="7f993-123">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="7f993-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="7f993-124">-Confirm</span></span>
<span data-ttu-id="7f993-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7f993-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f993-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f993-126">-WhatIf</span></span>
<span data-ttu-id="7f993-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7f993-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f993-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7f993-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f993-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f993-129">CommonParameters</span></span>
<span data-ttu-id="7f993-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7f993-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f993-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f993-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f993-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7f993-132">INPUTS</span></span>

### <span data-ttu-id="7f993-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f993-133">-ResourceGroupName</span></span>
 <span data-ttu-id="7f993-134">System. String</span><span class="sxs-lookup"><span data-stu-id="7f993-134">System.String</span></span>

### <span data-ttu-id="7f993-135">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="7f993-135">-NamespaceName</span></span>
 <span data-ttu-id="7f993-136">System. String</span><span class="sxs-lookup"><span data-stu-id="7f993-136">System.String</span></span>

### <span data-ttu-id="7f993-137">-Konum</span><span class="sxs-lookup"><span data-stu-id="7f993-137">-Location</span></span>
 <span data-ttu-id="7f993-138">System. String</span><span class="sxs-lookup"><span data-stu-id="7f993-138">System.String</span></span>

### <span data-ttu-id="7f993-139">-SkuName</span><span class="sxs-lookup"><span data-stu-id="7f993-139">-SkuName</span></span>
 <span data-ttu-id="7f993-140">System. String</span><span class="sxs-lookup"><span data-stu-id="7f993-140">System.String</span></span>

### <span data-ttu-id="7f993-141">Etiketli</span><span class="sxs-lookup"><span data-stu-id="7f993-141">-Tag</span></span>
 <span data-ttu-id="7f993-142">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7f993-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7f993-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7f993-143">OUTPUTS</span></span>

### <span data-ttu-id="7f993-144">Microsoft. Azure. Commands. Relay. modeller. RelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="7f993-144">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttributes</span></span>

## <span data-ttu-id="7f993-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7f993-145">NOTES</span></span>

## <span data-ttu-id="7f993-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7f993-146">RELATED LINKS</span></span>

