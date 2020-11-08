---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayNamespace.md
ms.openlocfilehash: c99bea4bb2f5ce9a404f828a3694136882cbefde
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274693"
---
# <span data-ttu-id="ee982-101">New-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="ee982-101">New-AzRelayNamespace</span></span>

## <span data-ttu-id="ee982-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee982-102">SYNOPSIS</span></span>
<span data-ttu-id="ee982-103">Yeni bir geçiş ad alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ee982-103">Creates a new Relay namespace.</span></span>

## <span data-ttu-id="ee982-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ee982-104">SYNTAX</span></span>

```
New-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee982-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ee982-105">DESCRIPTION</span></span>
<span data-ttu-id="ee982-106">**New-AzRelayNamespace** cmdlet 'i yeni bir geçiş ad alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ee982-106">The **New-AzRelayNamespace** cmdlet creates a new Relay namespace.</span></span> <span data-ttu-id="ee982-107">Oluşturulduktan sonra, ad alanı kaynak bildirimi sabittir.</span><span class="sxs-lookup"><span data-stu-id="ee982-107">Once created, the namespace resource manifest is immutable.</span></span>

## <span data-ttu-id="ee982-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ee982-108">EXAMPLES</span></span>

### <span data-ttu-id="ee982-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ee982-109">Example 1</span></span>
```
PS C:\> New-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1 -Location "West US" -Tag @{Tag1="Tag1Value"}

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

<span data-ttu-id="ee982-110">Belirtilen kaynak grubunda yeni bir geçiş ad alanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ee982-110">Creates a new Relay namespace within the specified resource group.</span></span>

## <span data-ttu-id="ee982-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ee982-111">PARAMETERS</span></span>

### <span data-ttu-id="ee982-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee982-112">-DefaultProfile</span></span>
<span data-ttu-id="ee982-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ee982-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee982-114">-Konum</span><span class="sxs-lookup"><span data-stu-id="ee982-114">-Location</span></span>
<span data-ttu-id="ee982-115">Geçiş ad alanı konumu.</span><span class="sxs-lookup"><span data-stu-id="ee982-115">Relay Namespace Location.</span></span>

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

### <span data-ttu-id="ee982-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="ee982-116">-Name</span></span>
<span data-ttu-id="ee982-117">Geçiş ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="ee982-117">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="ee982-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee982-118">-ResourceGroupName</span></span>
<span data-ttu-id="ee982-119">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ee982-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="ee982-120">Etiketli</span><span class="sxs-lookup"><span data-stu-id="ee982-120">-Tag</span></span>
<span data-ttu-id="ee982-121">Kaynak etiketlerini temsil eden hashtables 'lar.</span><span class="sxs-lookup"><span data-stu-id="ee982-121">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="ee982-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="ee982-122">-Confirm</span></span>
<span data-ttu-id="ee982-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ee982-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee982-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee982-124">-WhatIf</span></span>
<span data-ttu-id="ee982-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ee982-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee982-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ee982-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee982-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee982-127">CommonParameters</span></span>
<span data-ttu-id="ee982-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ee982-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee982-129">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee982-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee982-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ee982-130">INPUTS</span></span>

### <span data-ttu-id="ee982-131">System. String</span><span class="sxs-lookup"><span data-stu-id="ee982-131">System.String</span></span>

### <span data-ttu-id="ee982-132">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ee982-132">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ee982-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ee982-133">OUTPUTS</span></span>

### <span data-ttu-id="ee982-134">Microsoft. Azure. Commands. Relay. modeller. PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="ee982-134">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="ee982-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ee982-135">NOTES</span></span>

## <span data-ttu-id="ee982-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ee982-136">RELATED LINKS</span></span>
