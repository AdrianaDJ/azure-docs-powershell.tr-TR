---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayNamespace.md
ms.openlocfilehash: 6076a7fd8a71708bb3bdafdee8f1dfb0650b7088
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107671"
---
# <span data-ttu-id="e4f6c-101">Set-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="e4f6c-101">Set-AzRelayNamespace</span></span>

## <span data-ttu-id="e4f6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4f6c-102">SYNOPSIS</span></span>
<span data-ttu-id="e4f6c-103">Var olan bir geçiş ad alanının açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e4f6c-103">Updates the description of an existing Relay namespace.</span></span>

## <span data-ttu-id="e4f6c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e4f6c-104">SYNTAX</span></span>

```
Set-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-InputObject <RelayNamespaceAttirbutesUpdateParameter>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4f6c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e4f6c-105">DESCRIPTION</span></span>
<span data-ttu-id="e4f6c-106">**Set-AzRelayNamespace** cmdlet 'i, kaynak grubundaki belirtilen geçiş ad alanının açıklamasını günceller.</span><span class="sxs-lookup"><span data-stu-id="e4f6c-106">The **Set-AzRelayNamespace** cmdlet updates the description of the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="e4f6c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e4f6c-107">EXAMPLES</span></span>

### <span data-ttu-id="e4f6c-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e4f6c-108">Example 1</span></span>
```
PS C:\> Set-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1 -Tag @{Tag2="Tag2Value"}

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

<span data-ttu-id="e4f6c-109">Geçiş ad alanını yeni bir açıklamayla güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e4f6c-109">Updates the Relay namespace with a new description.</span></span>

## <span data-ttu-id="e4f6c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e4f6c-110">PARAMETERS</span></span>

### <span data-ttu-id="e4f6c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4f6c-111">-DefaultProfile</span></span>
<span data-ttu-id="e4f6c-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e4f6c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4f6c-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4f6c-113">-InputObject</span></span>
<span data-ttu-id="e4f6c-114">Geçiş ad alanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="e4f6c-114">Relay Namespace object.</span></span>

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

### <span data-ttu-id="e4f6c-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="e4f6c-115">-Name</span></span>
<span data-ttu-id="e4f6c-116">Geçiş ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="e4f6c-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="e4f6c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4f6c-117">-ResourceGroupName</span></span>
<span data-ttu-id="e4f6c-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="e4f6c-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="e4f6c-119">Etiketli</span><span class="sxs-lookup"><span data-stu-id="e4f6c-119">-Tag</span></span>
<span data-ttu-id="e4f6c-120">Kaynak etiketini temsil eden hashtables 'lar.</span><span class="sxs-lookup"><span data-stu-id="e4f6c-120">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="e4f6c-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="e4f6c-121">-Confirm</span></span>
<span data-ttu-id="e4f6c-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e4f6c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4f6c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4f6c-123">-WhatIf</span></span>
<span data-ttu-id="e4f6c-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e4f6c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4f6c-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e4f6c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4f6c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4f6c-126">CommonParameters</span></span>
<span data-ttu-id="e4f6c-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e4f6c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4f6c-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4f6c-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4f6c-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e4f6c-129">INPUTS</span></span>

### <span data-ttu-id="e4f6c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e4f6c-130">System.String</span></span>

### <span data-ttu-id="e4f6c-131">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e4f6c-131">System.Collections.Hashtable</span></span>

### <span data-ttu-id="e4f6c-132">Microsoft. Azure. Commands. Relay. modeller. RelayNamespaceAttirbutesUpdateParameter</span><span class="sxs-lookup"><span data-stu-id="e4f6c-132">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter</span></span>

## <span data-ttu-id="e4f6c-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e4f6c-133">OUTPUTS</span></span>

### <span data-ttu-id="e4f6c-134">Microsoft. Azure. Commands. Relay. modeller. PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="e4f6c-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="e4f6c-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e4f6c-135">NOTES</span></span>

## <span data-ttu-id="e4f6c-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e4f6c-136">RELATED LINKS</span></span>
