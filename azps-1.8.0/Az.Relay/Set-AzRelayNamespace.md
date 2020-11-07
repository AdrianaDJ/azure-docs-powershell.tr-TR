---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayNamespace.md
ms.openlocfilehash: eb42dc22f972928405821e8468e5610fa9c4514f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759484"
---
# <span data-ttu-id="e8bbf-101">Set-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="e8bbf-101">Set-AzRelayNamespace</span></span>

## <span data-ttu-id="e8bbf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8bbf-102">SYNOPSIS</span></span>
<span data-ttu-id="e8bbf-103">Var olan bir geçiş ad alanının açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e8bbf-103">Updates the description of an existing Relay namespace.</span></span>

## <span data-ttu-id="e8bbf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e8bbf-104">SYNTAX</span></span>

```
Set-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-InputObject <RelayNamespaceAttirbutesUpdateParameter>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8bbf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e8bbf-105">DESCRIPTION</span></span>
<span data-ttu-id="e8bbf-106">**Set-AzRelayNamespace** cmdlet 'i, kaynak grubundaki belirtilen geçiş ad alanının açıklamasını günceller.</span><span class="sxs-lookup"><span data-stu-id="e8bbf-106">The **Set-AzRelayNamespace** cmdlet updates the description of the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="e8bbf-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e8bbf-107">EXAMPLES</span></span>

### <span data-ttu-id="e8bbf-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e8bbf-108">Example 1</span></span>
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

<span data-ttu-id="e8bbf-109">Geçiş ad alanını yeni bir açıklamayla güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e8bbf-109">Updates the Relay namespace with a new description.</span></span>

## <span data-ttu-id="e8bbf-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e8bbf-110">PARAMETERS</span></span>

### <span data-ttu-id="e8bbf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8bbf-111">-DefaultProfile</span></span>
<span data-ttu-id="e8bbf-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e8bbf-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8bbf-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8bbf-113">-InputObject</span></span>
<span data-ttu-id="e8bbf-114">Geçiş ad alanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="e8bbf-114">Relay Namespace object.</span></span>

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

### <span data-ttu-id="e8bbf-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="e8bbf-115">-Name</span></span>
<span data-ttu-id="e8bbf-116">Geçiş ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="e8bbf-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="e8bbf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8bbf-117">-ResourceGroupName</span></span>
<span data-ttu-id="e8bbf-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="e8bbf-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="e8bbf-119">Etiketli</span><span class="sxs-lookup"><span data-stu-id="e8bbf-119">-Tag</span></span>
<span data-ttu-id="e8bbf-120">Kaynak etiketini temsil eden hashtables 'lar.</span><span class="sxs-lookup"><span data-stu-id="e8bbf-120">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="e8bbf-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="e8bbf-121">-Confirm</span></span>
<span data-ttu-id="e8bbf-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e8bbf-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8bbf-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8bbf-123">-WhatIf</span></span>
<span data-ttu-id="e8bbf-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e8bbf-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8bbf-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e8bbf-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8bbf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8bbf-126">CommonParameters</span></span>
<span data-ttu-id="e8bbf-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e8bbf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8bbf-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8bbf-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8bbf-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e8bbf-129">INPUTS</span></span>

### <span data-ttu-id="e8bbf-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e8bbf-130">System.String</span></span>

### <span data-ttu-id="e8bbf-131">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e8bbf-131">System.Collections.Hashtable</span></span>

### <span data-ttu-id="e8bbf-132">Microsoft. Azure. Commands. Relay. modeller. RelayNamespaceAttirbutesUpdateParameter</span><span class="sxs-lookup"><span data-stu-id="e8bbf-132">Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttirbutesUpdateParameter</span></span>

## <span data-ttu-id="e8bbf-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e8bbf-133">OUTPUTS</span></span>

### <span data-ttu-id="e8bbf-134">Microsoft. Azure. Commands. Relay. modeller. PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="e8bbf-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="e8bbf-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e8bbf-135">NOTES</span></span>

## <span data-ttu-id="e8bbf-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e8bbf-136">RELATED LINKS</span></span>