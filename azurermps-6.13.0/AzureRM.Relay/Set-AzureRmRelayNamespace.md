---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/set-azurermrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayNamespace.md
ms.openlocfilehash: 6bb333de426236099bed7402fc4756181415c4ec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762292"
---
# <span data-ttu-id="88e42-101">Set-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="88e42-101">Set-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="88e42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88e42-102">SYNOPSIS</span></span>
<span data-ttu-id="88e42-103">Var olan bir geçiş ad alanının açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="88e42-103">Updates the description of an existing Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88e42-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="88e42-104">SYNTAX</span></span>

```
Set-AzureRmRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-InputObject <RelayNamespaceAttirbutesUpdateParameter>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88e42-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="88e42-105">DESCRIPTION</span></span>
<span data-ttu-id="88e42-106">**Set-AzureRmRelayNamespace** cmdlet 'i, kaynak grubundaki belirtilen geçiş ad alanının açıklamasını günceller.</span><span class="sxs-lookup"><span data-stu-id="88e42-106">The **Set-AzureRmRelayNamespace** cmdlet updates the description of the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="88e42-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="88e42-107">EXAMPLES</span></span>

### <span data-ttu-id="88e42-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="88e42-108">Example 1</span></span>
```
PS C:\> Set-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1 -Tag @{Tag2="Tag2Value"}

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

<span data-ttu-id="88e42-109">Geçiş ad alanını yeni bir açıklamayla güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="88e42-109">Updates the Relay namespace with a new description.</span></span>

## <span data-ttu-id="88e42-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="88e42-110">PARAMETERS</span></span>

### <span data-ttu-id="88e42-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88e42-111">-DefaultProfile</span></span>
<span data-ttu-id="88e42-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="88e42-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88e42-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88e42-113">-InputObject</span></span>
<span data-ttu-id="88e42-114">Geçiş ad alanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="88e42-114">Relay Namespace object.</span></span>

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

### <span data-ttu-id="88e42-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="88e42-115">-Name</span></span>
<span data-ttu-id="88e42-116">Geçiş ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="88e42-116">Relay Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88e42-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88e42-117">-ResourceGroupName</span></span>
<span data-ttu-id="88e42-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="88e42-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="88e42-119">Etiketli</span><span class="sxs-lookup"><span data-stu-id="88e42-119">-Tag</span></span>
<span data-ttu-id="88e42-120">Kaynak etiketini temsil eden hashtables 'lar.</span><span class="sxs-lookup"><span data-stu-id="88e42-120">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="88e42-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="88e42-121">-Confirm</span></span>
<span data-ttu-id="88e42-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="88e42-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88e42-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88e42-123">-WhatIf</span></span>
<span data-ttu-id="88e42-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="88e42-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88e42-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="88e42-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88e42-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88e42-126">CommonParameters</span></span>
<span data-ttu-id="88e42-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="88e42-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="88e42-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88e42-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88e42-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="88e42-129">INPUTS</span></span>

### <span data-ttu-id="88e42-130">System. String</span><span class="sxs-lookup"><span data-stu-id="88e42-130">System.String</span></span>
<span data-ttu-id="88e42-131">System. topluluklar. Hashtable Microsoft. Azure. Commands. Relay. modeller. RelayNamespaceAttirbutesUpdateParameter</span><span class="sxs-lookup"><span data-stu-id="88e42-131">System.Collections.Hashtable Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter</span></span>


## <span data-ttu-id="88e42-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="88e42-132">OUTPUTS</span></span>

### <span data-ttu-id="88e42-133">Microsoft. Azure. Commands. Relay. modeller. PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="88e42-133">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>


## <span data-ttu-id="88e42-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="88e42-134">NOTES</span></span>

## <span data-ttu-id="88e42-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="88e42-135">RELATED LINKS</span></span>
