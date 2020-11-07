---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzWcfRelay.md
ms.openlocfilehash: 04925f904861eea006c6480dbdb48794afc55c56
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933381"
---
# <span data-ttu-id="4a1ce-101">Set-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="4a1ce-101">Set-AzWcfRelay</span></span>

## <span data-ttu-id="4a1ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a1ce-102">SYNOPSIS</span></span>
<span data-ttu-id="4a1ce-103">Belirtilen geçiş ad alanındaki WcfRelay 'in açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4a1ce-103">Updates the description of a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="4a1ce-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4a1ce-104">SYNTAX</span></span>

### <span data-ttu-id="4a1ce-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4a1ce-105">WcfRelayInputObjectSet</span></span>
```
Set-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSWcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4a1ce-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="4a1ce-106">WcfRelayPropertiesSet</span></span>
```
Set-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-UserMetadata <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a1ce-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4a1ce-107">DESCRIPTION</span></span>
<span data-ttu-id="4a1ce-108">Set-AzWcfRelay cmdlet 'i belirtilen geçiş ad alanındaki WcfRelay 'in açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4a1ce-108">The Set-AzWcfRelay cmdlet updates the description for the WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="4a1ce-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4a1ce-109">EXAMPLES</span></span>

### <span data-ttu-id="4a1ce-110">Örnek 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a1ce-110">Example 1 - InputObject</span></span>
```
PS C:\>
PS C:\> $getWcfRelay = Get-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay
PS C:\> $getWcfRelay.UserMetadata = "usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc
riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored."
PS C:\> Set-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -InputObject $getWcfRelay

RelayType                   : Http
CreatedAt                   : 4/26/2017 5:14:46 PM
UpdatedAt                   : 4/26/2017 5:16:50 PM
ListenerCount               :
RequiresClientAuthorization : False
RequiresTransportSecurity   : True
IsDynamic                   : False
UserMetadata                : usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc
riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel
                              ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2
Name                        : TestWCFRelay2
Type                        : Microsoft.Relay/WcfRelays
```

### <span data-ttu-id="4a1ce-111">Örnek 2-Özellikler</span><span class="sxs-lookup"><span data-stu-id="4a1ce-111">Example 2 - Properties</span></span>
```
PS C:\> Set-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -UserMetadata "User Meta data"

RelayType                   : NetTcp
CreatedAt                   : 4/26/2017 5:20:08 PM
UpdatedAt                   : 4/26/2017 5:26:09 PM
ListenerCount               :
RequiresClientAuthorization : True
RequiresTransportSecurity   : True
IsDynamic                   : False
UserMetadata                : User Meta data
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel
                              ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay
Name                        : TestWCFRelay
Type                        : Microsoft.Relay/WcfRelays
```

<span data-ttu-id="4a1ce-112">Belirtilen WcfRelay 'i belirtilen ad alanındaki yeni bir açıklamayla güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4a1ce-112">Updates the specified WcfRelay with a new description in the specified namespace.</span></span>
<span data-ttu-id="4a1ce-113">Bu örnek, yeni değeri olan UserMetadata özelliğini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4a1ce-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="4a1ce-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4a1ce-114">PARAMETERS</span></span>

### <span data-ttu-id="4a1ce-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a1ce-115">-DefaultProfile</span></span>
<span data-ttu-id="4a1ce-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4a1ce-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a1ce-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a1ce-117">-InputObject</span></span>
<span data-ttu-id="4a1ce-118">WcfRelay nesnesi.</span><span class="sxs-lookup"><span data-stu-id="4a1ce-118">WcfRelay object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes
Parameter Sets: WcfRelayInputObjectSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a1ce-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="4a1ce-119">-Name</span></span>
<span data-ttu-id="4a1ce-120">WcfRelay adı.</span><span class="sxs-lookup"><span data-stu-id="4a1ce-120">WcfRelay Name.</span></span>

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

### <span data-ttu-id="4a1ce-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4a1ce-121">-Namespace</span></span>
<span data-ttu-id="4a1ce-122">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="4a1ce-122">Namespace Name.</span></span>

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

### <span data-ttu-id="4a1ce-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a1ce-123">-ResourceGroupName</span></span>
<span data-ttu-id="4a1ce-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="4a1ce-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="4a1ce-125">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="4a1ce-125">-UserMetadata</span></span>
<span data-ttu-id="4a1ce-126">Usermetadata alır veya ayarlar, WcfRelay uç noktası için Kullanıcı tanımlı dize verilerinin depolanacağı bir yer tutucudur. ekip listesi ve kişi bilgileri gibi açıklayıcı verileri depolamak için kullanılabilir, Kullanıcı tanımlı yapılandırma ayarları da depolanabilir.</span><span class="sxs-lookup"><span data-stu-id="4a1ce-126">Gets or sets usermetadata is a placeholder to store user-defined string data for the WcfRelay endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a1ce-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="4a1ce-127">-Confirm</span></span>
<span data-ttu-id="4a1ce-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4a1ce-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a1ce-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a1ce-129">-WhatIf</span></span>
<span data-ttu-id="4a1ce-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4a1ce-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a1ce-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4a1ce-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a1ce-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a1ce-132">CommonParameters</span></span>
<span data-ttu-id="4a1ce-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4a1ce-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a1ce-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a1ce-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a1ce-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4a1ce-135">INPUTS</span></span>

### <span data-ttu-id="4a1ce-136">System. String</span><span class="sxs-lookup"><span data-stu-id="4a1ce-136">System.String</span></span>

### <span data-ttu-id="4a1ce-137">Microsoft. Azure. Commands. Relay. modeller. PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="4a1ce-137">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="4a1ce-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4a1ce-138">OUTPUTS</span></span>

### <span data-ttu-id="4a1ce-139">Microsoft. Azure. Commands. Relay. modeller. PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="4a1ce-139">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="4a1ce-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4a1ce-140">NOTES</span></span>

## <span data-ttu-id="4a1ce-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4a1ce-141">RELATED LINKS</span></span>
