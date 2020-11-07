---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayNamespace.md
ms.openlocfilehash: 365a80e1ddf5673be5c45c5d17b24490c277a365
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763636"
---
# <span data-ttu-id="8e974-101">New-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="8e974-101">New-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="8e974-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e974-102">SYNOPSIS</span></span>
<span data-ttu-id="8e974-103">Yeni bir geçiş ad alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8e974-103">Creates a new Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e974-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8e974-104">SYNTAX</span></span>

```
New-AzureRmRelayNamespace [-ResourceGroupName] <String> -Name <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e974-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8e974-105">DESCRIPTION</span></span>
<span data-ttu-id="8e974-106">**New-AzureRmRelayNamespace** cmdlet 'i yeni bir geçiş ad alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8e974-106">The **New-AzureRmRelayNamespace** cmdlet creates a new Relay namespace.</span></span> <span data-ttu-id="8e974-107">Oluşturulduktan sonra, ad alanı kaynak bildirimi sabittir.</span><span class="sxs-lookup"><span data-stu-id="8e974-107">Once created, the namespace resource manifest is immutable.</span></span>

## <span data-ttu-id="8e974-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8e974-108">EXAMPLES</span></span>

### <span data-ttu-id="8e974-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8e974-109">Example 1</span></span>
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

<span data-ttu-id="8e974-110">Belirtilen kaynak grubunda yeni bir geçiş ad alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8e974-110">Creates a new Relay namespace within the specified resource group.</span></span>

## <span data-ttu-id="8e974-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8e974-111">PARAMETERS</span></span>

### <span data-ttu-id="8e974-112">-Konum</span><span class="sxs-lookup"><span data-stu-id="8e974-112">-Location</span></span>
<span data-ttu-id="8e974-113">Geçiş ad alanı konumu.</span><span class="sxs-lookup"><span data-stu-id="8e974-113">Relay Namespace Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e974-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e974-114">-ResourceGroupName</span></span>
<span data-ttu-id="8e974-115">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="8e974-115">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e974-116">Etiketli</span><span class="sxs-lookup"><span data-stu-id="8e974-116">-Tag</span></span>
<span data-ttu-id="8e974-117">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="8e974-117">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8e974-118">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="8e974-118">For example:</span></span>

<span data-ttu-id="8e974-119">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="8e974-119">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e974-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="8e974-120">-Confirm</span></span>
<span data-ttu-id="8e974-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8e974-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e974-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e974-122">-WhatIf</span></span>
<span data-ttu-id="8e974-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8e974-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e974-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8e974-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e974-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e974-125">-DefaultProfile</span></span>
<span data-ttu-id="8e974-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8e974-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e974-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="8e974-127">-Name</span></span>
<span data-ttu-id="8e974-128">Geçiş ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="8e974-128">Relay Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e974-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e974-129">CommonParameters</span></span>
<span data-ttu-id="8e974-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8e974-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e974-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e974-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e974-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8e974-132">INPUTS</span></span>

### <span data-ttu-id="8e974-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e974-133">-ResourceGroupName</span></span>
 <span data-ttu-id="8e974-134">System. String</span><span class="sxs-lookup"><span data-stu-id="8e974-134">System.String</span></span>

### <span data-ttu-id="8e974-135">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="8e974-135">-NamespaceName</span></span>
 <span data-ttu-id="8e974-136">System. String</span><span class="sxs-lookup"><span data-stu-id="8e974-136">System.String</span></span>

### <span data-ttu-id="8e974-137">-Konum</span><span class="sxs-lookup"><span data-stu-id="8e974-137">-Location</span></span>
 <span data-ttu-id="8e974-138">System. String</span><span class="sxs-lookup"><span data-stu-id="8e974-138">System.String</span></span>

### <span data-ttu-id="8e974-139">-SkuName</span><span class="sxs-lookup"><span data-stu-id="8e974-139">-SkuName</span></span>
 <span data-ttu-id="8e974-140">System. String</span><span class="sxs-lookup"><span data-stu-id="8e974-140">System.String</span></span>

### <span data-ttu-id="8e974-141">Etiketli</span><span class="sxs-lookup"><span data-stu-id="8e974-141">-Tag</span></span>
 <span data-ttu-id="8e974-142">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8e974-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8e974-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8e974-143">OUTPUTS</span></span>

### <span data-ttu-id="8e974-144">Microsoft. Azure. Commands. Relay. modeller. RelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="8e974-144">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttributes</span></span>

## <span data-ttu-id="8e974-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8e974-145">NOTES</span></span>

## <span data-ttu-id="8e974-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8e974-146">RELATED LINKS</span></span>

