---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayHybridConnection.md
ms.openlocfilehash: 2b029b2a93a063a322c11ea84cd46b787acc9960
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938147"
---
# <span data-ttu-id="0e7e4-101">Set-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="0e7e4-101">Set-AzRelayHybridConnection</span></span>

## <span data-ttu-id="0e7e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e7e4-102">SYNOPSIS</span></span>
<span data-ttu-id="0e7e4-103">Belirtilen geçiş ad alanındaki bir HybridConnection açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="0e7e4-103">Updates the description of a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="0e7e4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0e7e4-104">SYNTAX</span></span>

### <span data-ttu-id="0e7e4-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0e7e4-105">HybridConnectionInputObjectSet</span></span>
```
Set-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSHybridConnectionAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0e7e4-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="0e7e4-106">HybridConnectionPropertiesSet</span></span>
```
Set-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e7e4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0e7e4-107">DESCRIPTION</span></span>
<span data-ttu-id="0e7e4-108">Set-AzRelayHybridConnection cmdlet 'i, belirtilen geçiş ad alanındaki HybridConnection öğesinin açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="0e7e4-108">The Set-AzRelayHybridConnection cmdlet updates the description for the HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="0e7e4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0e7e4-109">EXAMPLES</span></span>

### <span data-ttu-id="0e7e4-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0e7e4-110">Example 1</span></span>
```
PS C:\>
PS C:\> $GetHybrid = Get-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
PS C:\> $GetHybrid.UserMetadata = "Test UserMetadata"
PS C:\> Set-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection -InputObject $GetHybrid

CreatedAt                   : 4/26/2017 10:04:15 PM
UpdatedAt                   : 4/26/2017 10:08:11 PM
ListenerCount               :
RequiresClientAuthorization : True
UserMetadata                : Test UserMetadata
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS
                              /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio
                              n2
Name                        : TestHybirdConnection2
Type                        : Microsoft.Relay/HybridConnections
```

### <span data-ttu-id="0e7e4-111">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="0e7e4-111">Example 2</span></span>
```
PS C:\> Set-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection -UserMetadata = "Test UserMetadata updated"

CreatedAt                   : 4/26/2017 10:04:15 PM
UpdatedAt                   : 4/26/2017 10:10:25 PM
ListenerCount               :
RequiresClientAuthorization : True
UserMetadata                : Test UserMetadata updated
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS
                              /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio
                              n1
Name                        : TestHybirdConnection1
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="0e7e4-112">Belirtilen HybridConnection öğesini belirtilen ad alanındaki yeni bir açıklamayla güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="0e7e4-112">Updates the specified HybridConnection with a new description in the specified namespace.</span></span>
<span data-ttu-id="0e7e4-113">Bu örnek, yeni değeri olan UserMetadata özelliğini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="0e7e4-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="0e7e4-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0e7e4-114">PARAMETERS</span></span>

### <span data-ttu-id="0e7e4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e7e4-115">-DefaultProfile</span></span>
<span data-ttu-id="0e7e4-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0e7e4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e7e4-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0e7e4-117">-InputObject</span></span>
<span data-ttu-id="0e7e4-118">HybridConnections nesnesi.</span><span class="sxs-lookup"><span data-stu-id="0e7e4-118">HybridConnections object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes
Parameter Sets: HybridConnectionInputObjectSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e7e4-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="0e7e4-119">-Name</span></span>
<span data-ttu-id="0e7e4-120">HybridConnections adı.</span><span class="sxs-lookup"><span data-stu-id="0e7e4-120">HybridConnections Name.</span></span>

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

### <span data-ttu-id="0e7e4-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0e7e4-121">-Namespace</span></span>
<span data-ttu-id="0e7e4-122">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="0e7e4-122">Namespace Name.</span></span>

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

### <span data-ttu-id="0e7e4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e7e4-123">-ResourceGroupName</span></span>
<span data-ttu-id="0e7e4-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="0e7e4-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="0e7e4-125">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="0e7e4-125">-UserMetadata</span></span>
<span data-ttu-id="0e7e4-126">Kullanıcı tanımlı dize verilerinin HybridConnection uç noktasına depolanması için bir yer tutucudur. ekip listesi ve kişi bilgileri gibi açıklayıcı verileri depolamak için kullanılabilir, Kullanıcı tanımlı yapılandırma ayarları da depolanabilir.</span><span class="sxs-lookup"><span data-stu-id="0e7e4-126">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e7e4-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="0e7e4-127">-Confirm</span></span>
<span data-ttu-id="0e7e4-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0e7e4-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e7e4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e7e4-129">-WhatIf</span></span>
<span data-ttu-id="0e7e4-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0e7e4-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e7e4-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0e7e4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e7e4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e7e4-132">CommonParameters</span></span>
<span data-ttu-id="0e7e4-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0e7e4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e7e4-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e7e4-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e7e4-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0e7e4-135">INPUTS</span></span>

### <span data-ttu-id="0e7e4-136">System. String</span><span class="sxs-lookup"><span data-stu-id="0e7e4-136">System.String</span></span>

### <span data-ttu-id="0e7e4-137">Microsoft. Azure. Commands. Relay. modeller. PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="0e7e4-137">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="0e7e4-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0e7e4-138">OUTPUTS</span></span>

### <span data-ttu-id="0e7e4-139">Microsoft. Azure. Commands. Relay. modeller. PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="0e7e4-139">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="0e7e4-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0e7e4-140">NOTES</span></span>

## <span data-ttu-id="0e7e4-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0e7e4-141">RELATED LINKS</span></span>