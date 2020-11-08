---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayHybridConnection.md
ms.openlocfilehash: 04022129d6709cf7dceea128b2813f97a5404234
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268380"
---
# <span data-ttu-id="04228-101">New-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="04228-101">New-AzRelayHybridConnection</span></span>

## <span data-ttu-id="04228-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04228-102">SYNOPSIS</span></span>
<span data-ttu-id="04228-103">Belirtilen geçiş ad alanında HybridConnection oluşturur.</span><span class="sxs-lookup"><span data-stu-id="04228-103">Creates a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="04228-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="04228-104">SYNTAX</span></span>

### <span data-ttu-id="04228-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="04228-105">HybridConnectionInputObjectSet</span></span>
```
New-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSHybridConnectionAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="04228-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="04228-106">HybridConnectionPropertiesSet</span></span>
```
New-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RequiresClientAuthorization <Boolean>] [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04228-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="04228-107">DESCRIPTION</span></span>
<span data-ttu-id="04228-108">New-AzRelayHybridConnection cmdlet 'i belirtilen geçiş ad boşluğunda bir HybridConnection oluşturur.</span><span class="sxs-lookup"><span data-stu-id="04228-108">The New-AzRelayHybridConnection cmdlet creates a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="04228-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="04228-109">EXAMPLES</span></span>

### <span data-ttu-id="04228-110">Örnek 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="04228-110">Example 1 - InputObject</span></span>
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

<span data-ttu-id="04228-111">\` \` Belirtilen geçiş ad alanı \` TestNamespace-hybirvseçconnection 'Da yeni bir hybirvseçconnection TestHybirdConnection2 oluşturur \` .</span><span class="sxs-lookup"><span data-stu-id="04228-111">Creates a new HybirdConnection \`TestHybirdConnection2\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

### <span data-ttu-id="04228-112">Örnek 2-Özellikler</span><span class="sxs-lookup"><span data-stu-id="04228-112">Example 2 - Properties</span></span>
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

<span data-ttu-id="04228-113">\` \` Belirtilen geçiş ad alanı \` TestNamespace-hybirvseçconnection 'Da yeni bir hybirvseçconnection TestHybirdConnection1 oluşturur \` .</span><span class="sxs-lookup"><span data-stu-id="04228-113">Creates a new HybirdConnection \`TestHybirdConnection1\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

## <span data-ttu-id="04228-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="04228-114">PARAMETERS</span></span>

### <span data-ttu-id="04228-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04228-115">-DefaultProfile</span></span>
<span data-ttu-id="04228-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="04228-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04228-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04228-117">-InputObject</span></span>
<span data-ttu-id="04228-118">HybridConnections nesnesi.</span><span class="sxs-lookup"><span data-stu-id="04228-118">HybridConnections object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes
Parameter Sets: HybridConnectionInputObjectSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04228-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="04228-119">-Name</span></span>
<span data-ttu-id="04228-120">HybridConnections adı.</span><span class="sxs-lookup"><span data-stu-id="04228-120">HybridConnections Name.</span></span>

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

### <span data-ttu-id="04228-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="04228-121">-Namespace</span></span>
<span data-ttu-id="04228-122">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="04228-122">Namespace Name.</span></span>

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

### <span data-ttu-id="04228-123">-Requiresclientauthorter</span><span class="sxs-lookup"><span data-stu-id="04228-123">-RequiresClientAuthorization</span></span>
<span data-ttu-id="04228-124">Bu HybridConnections için istemci yetkilendirmesi gerekliyse doğru; Aksi takdirde, false</span><span class="sxs-lookup"><span data-stu-id="04228-124">true if client authorization is needed for this HybridConnections; otherwise, false</span></span>

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

### <span data-ttu-id="04228-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04228-125">-ResourceGroupName</span></span>
<span data-ttu-id="04228-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="04228-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="04228-127">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="04228-127">-UserMetadata</span></span>
<span data-ttu-id="04228-128">Kullanıcı tanımlı dize verilerinin HybridConnection uç noktasına depolanması için bir yer tutucudur. ekip listesi ve kişi bilgileri gibi açıklayıcı verileri depolamak için kullanılabilir, Kullanıcı tanımlı yapılandırma ayarları da depolanabilir.</span><span class="sxs-lookup"><span data-stu-id="04228-128">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="04228-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="04228-129">-Confirm</span></span>
<span data-ttu-id="04228-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="04228-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04228-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04228-131">-WhatIf</span></span>
<span data-ttu-id="04228-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="04228-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04228-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="04228-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04228-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04228-134">CommonParameters</span></span>
<span data-ttu-id="04228-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="04228-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04228-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04228-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04228-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="04228-137">INPUTS</span></span>

### <span data-ttu-id="04228-138">System. String</span><span class="sxs-lookup"><span data-stu-id="04228-138">System.String</span></span>

### <span data-ttu-id="04228-139">Microsoft. Azure. Commands. Relay. modeller. PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="04228-139">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

### <span data-ttu-id="04228-140">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="04228-140">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="04228-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="04228-141">OUTPUTS</span></span>

### <span data-ttu-id="04228-142">Microsoft. Azure. Commands. Relay. modeller. PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="04228-142">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="04228-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="04228-143">NOTES</span></span>

## <span data-ttu-id="04228-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="04228-144">RELATED LINKS</span></span>
