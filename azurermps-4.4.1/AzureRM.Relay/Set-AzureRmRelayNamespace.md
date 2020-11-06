---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayNamespace.md
ms.openlocfilehash: c243f31ee549443ad959bde13abc9ff3b68c1560
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589134"
---
# <span data-ttu-id="55b03-101">Set-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="55b03-101">Set-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="55b03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55b03-102">SYNOPSIS</span></span>
<span data-ttu-id="55b03-103">Var olan bir geçiş ad alanının açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="55b03-103">Updates the description of an existing Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55b03-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="55b03-104">SYNTAX</span></span>

```
Set-AzureRmRelayNamespace [-ResourceGroupName] <String> -Name <String> [-Tag <Hashtable>]
 [-InputObject <RelayNamespaceAttirbutesUpdateParameter>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55b03-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="55b03-105">DESCRIPTION</span></span>
<span data-ttu-id="55b03-106">**Set-AzureRmRelayNamespace** cmdlet 'i, kaynak grubundaki belirtilen geçiş ad alanının açıklamasını günceller.</span><span class="sxs-lookup"><span data-stu-id="55b03-106">The **Set-AzureRmRelayNamespace** cmdlet updates the description of the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="55b03-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="55b03-107">EXAMPLES</span></span>

### <span data-ttu-id="55b03-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="55b03-108">Example 1</span></span>
```
PS C:\> Set-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Tag @{Tag2="Tag2Value"}

ProvisioningState  :
CreatedAt          : 4/12/2017 12:38:47 AM
UpdatedAt          : 4/12/2017 12:39:10 AM
ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/
MetricId           :
Location           :
Tags               : {[tag2, Tag2Value]}
Id                 :
Name               :
Type               :
```

<span data-ttu-id="55b03-109">Geçiş ad alanını yeni bir açıklamayla güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="55b03-109">Updates the Relay namespace with a new description.</span></span>

## <span data-ttu-id="55b03-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="55b03-110">PARAMETERS</span></span>

### <span data-ttu-id="55b03-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55b03-111">-ResourceGroupName</span></span>
<span data-ttu-id="55b03-112">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="55b03-112">Resource Group Name.</span></span>

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

### <span data-ttu-id="55b03-113">Etiketli</span><span class="sxs-lookup"><span data-stu-id="55b03-113">-Tag</span></span>
<span data-ttu-id="55b03-114">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="55b03-114">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="55b03-115">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="55b03-115">For example:</span></span>

<span data-ttu-id="55b03-116">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="55b03-116">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="55b03-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="55b03-117">-Confirm</span></span>
<span data-ttu-id="55b03-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="55b03-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55b03-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55b03-119">-WhatIf</span></span>
<span data-ttu-id="55b03-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="55b03-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55b03-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="55b03-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55b03-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55b03-122">-DefaultProfile</span></span>
<span data-ttu-id="55b03-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="55b03-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55b03-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55b03-124">-InputObject</span></span>
<span data-ttu-id="55b03-125">Geçiş ad alanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="55b03-125">Relay Namespace object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55b03-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="55b03-126">-Name</span></span>
<span data-ttu-id="55b03-127">Geçiş ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="55b03-127">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="55b03-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55b03-128">CommonParameters</span></span>
<span data-ttu-id="55b03-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="55b03-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55b03-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55b03-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55b03-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="55b03-131">INPUTS</span></span>

### <span data-ttu-id="55b03-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55b03-132">-ResourceGroupName</span></span>
 <span data-ttu-id="55b03-133">System. String</span><span class="sxs-lookup"><span data-stu-id="55b03-133">System.String</span></span>

### <span data-ttu-id="55b03-134">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="55b03-134">-NamespaceName</span></span>
 <span data-ttu-id="55b03-135">System. String</span><span class="sxs-lookup"><span data-stu-id="55b03-135">System.String</span></span>

### <span data-ttu-id="55b03-136">-Konum</span><span class="sxs-lookup"><span data-stu-id="55b03-136">-Location</span></span>
 <span data-ttu-id="55b03-137">System. String</span><span class="sxs-lookup"><span data-stu-id="55b03-137">System.String</span></span>

### <span data-ttu-id="55b03-138">Etiketli</span><span class="sxs-lookup"><span data-stu-id="55b03-138">-Tag</span></span>
 <span data-ttu-id="55b03-139">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="55b03-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="55b03-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="55b03-140">OUTPUTS</span></span>

### <span data-ttu-id="55b03-141">Microsoft. Azure. Commands. Relay. modeller. RelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="55b03-141">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttributes</span></span>

## <span data-ttu-id="55b03-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="55b03-142">NOTES</span></span>

## <span data-ttu-id="55b03-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="55b03-143">RELATED LINKS</span></span>

