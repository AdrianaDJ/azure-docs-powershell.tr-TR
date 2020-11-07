---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayHybridConnection.md
ms.openlocfilehash: 9f0145cee1facbd409406b86b2a6fc15f034737a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759506"
---
# <span data-ttu-id="e8270-101">New-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="e8270-101">New-AzRelayHybridConnection</span></span>

## <span data-ttu-id="e8270-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8270-102">SYNOPSIS</span></span>
<span data-ttu-id="e8270-103">Belirtilen geçiş ad alanında HybridConnection oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e8270-103">Creates a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="e8270-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e8270-104">SYNTAX</span></span>

### <span data-ttu-id="e8270-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e8270-105">HybridConnectionInputObjectSet</span></span>
```
New-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSHybridConnectionAttibutes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e8270-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="e8270-106">HybridConnectionPropertiesSet</span></span>
```
New-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RequiresClientAuthorization <Boolean>] [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8270-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e8270-107">DESCRIPTION</span></span>
<span data-ttu-id="e8270-108">New-AzRelayHybridConnection cmdlet 'i belirtilen geçiş ad boşluğunda bir HybridConnection oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e8270-108">The New-AzRelayHybridConnection cmdlet creates a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="e8270-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e8270-109">EXAMPLES</span></span>

### <span data-ttu-id="e8270-110">Örnek 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8270-110">Example 1 - InputObject</span></span>
```
PS C:\> $getHybirdConnection = Get-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-HybirdConnection -Name TestHybirdConnection1
PS C:\> $getHybirdConnection.UserMetadata = "TestHybirdConnection2"
PS C:\> $getHybirdConnection.RequiresClientAuthorization = $False
PS C:\> New-AzRelayHybridConnection -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection2 -InputObject $getHybirdConnection

CreatedAt                   : 4/26/2017 10:04:15 PM
UpdatedAt                   : 4/26/2017 10:04:15 PM
ListenerCount               :
RequiresClientAuthorization : True
UserMetadata                : User Meta data
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS
                              /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio
                              n2
Name                        : TestHybirdConnection2
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="e8270-111">\` \` Belirtilen geçiş ad alanı \` TestNamespace-hybirvseçconnection 'Da yeni bir hybirvseçconnection TestHybirdConnection2 oluşturur \` .</span><span class="sxs-lookup"><span data-stu-id="e8270-111">Creates a new HybirdConnection \`TestHybirdConnection2\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

### <span data-ttu-id="e8270-112">Örnek 2-Özellikler</span><span class="sxs-lookup"><span data-stu-id="e8270-112">Example 2 - Properties</span></span>
```
PS C:\> New-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection1 -RequiresClientAuthorization $True -UserMetadata "User Meta data"

CreatedAt                   : 4/26/2017 10:04:15 PM
UpdatedAt                   : 4/26/2017 10:04:15 PM
ListenerCount               :
RequiresClientAuthorization : True
UserMetadata                : User Meta data
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS
                              /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio
                              n1
Name                        : TestHybirdConnection1
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="e8270-113">\` \` Belirtilen geçiş ad alanı \` TestNamespace-hybirvseçconnection 'Da yeni bir hybirvseçconnection TestHybirdConnection1 oluşturur \` .</span><span class="sxs-lookup"><span data-stu-id="e8270-113">Creates a new HybirdConnection \`TestHybirdConnection1\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

## <span data-ttu-id="e8270-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e8270-114">PARAMETERS</span></span>

### <span data-ttu-id="e8270-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8270-115">-DefaultProfile</span></span>
<span data-ttu-id="e8270-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e8270-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8270-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8270-117">-InputObject</span></span>
<span data-ttu-id="e8270-118">HybridConnections nesnesi.</span><span class="sxs-lookup"><span data-stu-id="e8270-118">HybridConnections object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttibutes
Parameter Sets: HybridConnectionInputObjectSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8270-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="e8270-119">-Name</span></span>
<span data-ttu-id="e8270-120">HybridConnections adı.</span><span class="sxs-lookup"><span data-stu-id="e8270-120">HybridConnections Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8270-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e8270-121">-Namespace</span></span>
<span data-ttu-id="e8270-122">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="e8270-122">Namespace Name.</span></span>

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

### <span data-ttu-id="e8270-123">-Requiresclientauthorter</span><span class="sxs-lookup"><span data-stu-id="e8270-123">-RequiresClientAuthorization</span></span>
<span data-ttu-id="e8270-124">Bu HybridConnections için istemci yetkilendirmesi gerekliyse doğru; Aksi takdirde, false</span><span class="sxs-lookup"><span data-stu-id="e8270-124">true if client authorization is needed for this HybridConnections; otherwise, false</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: HybridConnectionPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8270-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8270-125">-ResourceGroupName</span></span>
<span data-ttu-id="e8270-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="e8270-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="e8270-127">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="e8270-127">-UserMetadata</span></span>
<span data-ttu-id="e8270-128">Kullanıcı tanımlı dize verilerinin HybridConnection uç noktasına depolanması için bir yer tutucudur. ekip listesi ve kişi bilgileri gibi açıklayıcı verileri depolamak için kullanılabilir, Kullanıcı tanımlı yapılandırma ayarları da depolanabilir.</span><span class="sxs-lookup"><span data-stu-id="e8270-128">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="e8270-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="e8270-129">-Confirm</span></span>
<span data-ttu-id="e8270-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e8270-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8270-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8270-131">-WhatIf</span></span>
<span data-ttu-id="e8270-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e8270-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8270-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e8270-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8270-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8270-134">CommonParameters</span></span>
<span data-ttu-id="e8270-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e8270-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8270-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8270-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8270-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e8270-137">INPUTS</span></span>

### <span data-ttu-id="e8270-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e8270-138">System.String</span></span>

### <span data-ttu-id="e8270-139">Microsoft. Azure. Commands. Relay. modeller. PSHybridConnectionAttibutes</span><span class="sxs-lookup"><span data-stu-id="e8270-139">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttibutes</span></span>

### <span data-ttu-id="e8270-140">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="e8270-140">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e8270-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e8270-141">OUTPUTS</span></span>

### <span data-ttu-id="e8270-142">Microsoft. Azure. Commands. Relay. modeller. PSHybridConnectionAttibutes</span><span class="sxs-lookup"><span data-stu-id="e8270-142">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttibutes</span></span>

## <span data-ttu-id="e8270-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e8270-143">NOTES</span></span>

## <span data-ttu-id="e8270-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e8270-144">RELATED LINKS</span></span>
