---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 315c50dbbc68865058f6c5663952fe2f42bc5c85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587804"
---
# <span data-ttu-id="79198-101">New-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="79198-101">New-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="79198-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79198-102">SYNOPSIS</span></span>
<span data-ttu-id="79198-103">Belirtilen geçiş ad alanında HybridConnection oluşturur.</span><span class="sxs-lookup"><span data-stu-id="79198-103">Creates a HybridConnection in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79198-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="79198-104">SYNTAX</span></span>

### <span data-ttu-id="79198-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="79198-105">HybridConnectionInputObjectSet</span></span>
```
New-AzureRmRelayHybridConnection -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-InputObject <HybridConnectionAttibutes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="79198-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="79198-106">HybridConnectionPropertiesSet</span></span>
```
New-AzureRmRelayHybridConnection -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-RequiresClientAuthorization <Boolean>] [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79198-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="79198-107">DESCRIPTION</span></span>
<span data-ttu-id="79198-108">New-AzureRmRelayHybridConnection cmdlet 'i belirtilen geçiş ad boşluğunda bir HybridConnection oluşturur.</span><span class="sxs-lookup"><span data-stu-id="79198-108">The New-AzureRmRelayHybridConnection cmdlet creates a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="79198-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="79198-109">EXAMPLES</span></span>

### <span data-ttu-id="79198-110">Örnek 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="79198-110">Example 1 - InputObject</span></span>
```
PS C:\> $getHybirdConnection = Get-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-HybirdConnection -Name TestHybirdConnection1
PS C:\> $getHybirdConnection.UserMetadata = "TestHybirdConnection2"
PS C:\> $getHybirdConnection.RequiresClientAuthorization = $False
PS C:\> New-AzureRmRelayHybridConnection -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection2 -InputObject $getHybirdConnection
```

<span data-ttu-id="79198-111">\` \` Belirtilen geçiş ad alanı \` TestNamespace-hybirvseçconnection 'Da yeni bir hybirvseçconnection TestHybirdConnection2 oluşturur \` .</span><span class="sxs-lookup"><span data-stu-id="79198-111">Creates a new HybirdConnection \`TestHybirdConnection2\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

### <span data-ttu-id="79198-112">Örnek 2-Özellikler</span><span class="sxs-lookup"><span data-stu-id="79198-112">Example 2 - Properties</span></span>
```
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection1 -RequiresClientAuthorization $True -UserMetadata "User Meta data"
```

<span data-ttu-id="79198-113">\` \` Belirtilen geçiş ad alanı \` TestNamespace-hybirvseçconnection 'Da yeni bir hybirvseçconnection TestHybirdConnection1 oluşturur \` .</span><span class="sxs-lookup"><span data-stu-id="79198-113">Creates a new HybirdConnection \`TestHybirdConnection1\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

## <span data-ttu-id="79198-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="79198-114">PARAMETERS</span></span>

### <span data-ttu-id="79198-115">-Requiresclientauthorter</span><span class="sxs-lookup"><span data-stu-id="79198-115">-RequiresClientAuthorization</span></span>
<span data-ttu-id="79198-116">Bu HybridConnections için istemci yetkilendirmesi gerekliyse doğru; Aksi takdirde, false</span><span class="sxs-lookup"><span data-stu-id="79198-116">true if client authorization is needed for this HybridConnections; otherwise, false</span></span>

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

### <span data-ttu-id="79198-117">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="79198-117">-UserMetadata</span></span>
<span data-ttu-id="79198-118">Kullanıcı tanımlı dize verilerinin HybridConnection uç noktasına depolanması için bir yer tutucudur. ekip listesi ve kişi bilgileri gibi açıklayıcı verileri depolamak için kullanılabilir, Kullanıcı tanımlı yapılandırma ayarları da depolanabilir.</span><span class="sxs-lookup"><span data-stu-id="79198-118">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="79198-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="79198-119">-Confirm</span></span>
<span data-ttu-id="79198-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="79198-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79198-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79198-121">-WhatIf</span></span>
<span data-ttu-id="79198-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="79198-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79198-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="79198-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79198-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="79198-124">-InputObject</span></span>
<span data-ttu-id="79198-125">HybridConnections nesnesi.</span><span class="sxs-lookup"><span data-stu-id="79198-125">HybridConnections object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes
Parameter Sets: HybridConnectionInputObjectSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79198-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="79198-126">-Name</span></span>
<span data-ttu-id="79198-127">HybridConnections adı.</span><span class="sxs-lookup"><span data-stu-id="79198-127">HybridConnections Name.</span></span>

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

### <span data-ttu-id="79198-128">-Namespace</span><span class="sxs-lookup"><span data-stu-id="79198-128">-Namespace</span></span>
<span data-ttu-id="79198-129">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="79198-129">Namespace Name.</span></span>

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

### <span data-ttu-id="79198-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79198-130">-ResourceGroupName</span></span>
<span data-ttu-id="79198-131">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="79198-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="79198-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79198-132">-DefaultProfile</span></span>
<span data-ttu-id="79198-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="79198-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79198-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79198-134">CommonParameters</span></span>
<span data-ttu-id="79198-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="79198-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79198-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79198-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79198-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="79198-137">INPUTS</span></span>

### <span data-ttu-id="79198-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79198-138">-ResourceGroupName</span></span>
<span data-ttu-id="79198-139">System. String</span><span class="sxs-lookup"><span data-stu-id="79198-139">System.String</span></span>

### <span data-ttu-id="79198-140">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="79198-140">-NamespaceName</span></span>
<span data-ttu-id="79198-141">System. String</span><span class="sxs-lookup"><span data-stu-id="79198-141">System.String</span></span>

### <span data-ttu-id="79198-142">-HybridConnectionsName</span><span class="sxs-lookup"><span data-stu-id="79198-142">-HybridConnectionsName</span></span>
<span data-ttu-id="79198-143">System. String</span><span class="sxs-lookup"><span data-stu-id="79198-143">System.String</span></span>

### <span data-ttu-id="79198-144">-InputObject</span><span class="sxs-lookup"><span data-stu-id="79198-144">-InputObject</span></span>
<span data-ttu-id="79198-145">Microsoft. Azure. Commands. Relay. modeller. HybridConnectionAttibutes</span><span class="sxs-lookup"><span data-stu-id="79198-145">Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes</span></span>

### <span data-ttu-id="79198-146">-Requiresclientauthorter</span><span class="sxs-lookup"><span data-stu-id="79198-146">-RequiresClientAuthorization</span></span>
<span data-ttu-id="79198-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="79198-147">System.Boolean</span></span>

### <span data-ttu-id="79198-148">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="79198-148">-UserMetadata</span></span>
<span data-ttu-id="79198-149">System. String</span><span class="sxs-lookup"><span data-stu-id="79198-149">System.String</span></span>

## <span data-ttu-id="79198-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="79198-150">OUTPUTS</span></span>

### <span data-ttu-id="79198-151">Microsoft. Azure. Commands. Relay. modeller. HybridConnectionAttibutes</span><span class="sxs-lookup"><span data-stu-id="79198-151">Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes</span></span>

### <span data-ttu-id="79198-152">Örnekler-1: InputObject</span><span class="sxs-lookup"><span data-stu-id="79198-152">Examples - 1 : InputObject</span></span>
<span data-ttu-id="79198-153">CreatedAt: 4/26/2017 10:04:15 PM UpdatedAt: 4/26/2017 10:04:15 PM ListenerCount: Requiresclientauthor,: TestHybirdConnection2 Type: Microsoft. Relay/HybridConnections</span><span class="sxs-lookup"><span data-stu-id="79198-153">CreatedAt                   : 4/26/2017 10:04:15 PM UpdatedAt                   : 4/26/2017 10:04:15 PM ListenerCount               : RequiresClientAuthorization : True UserMetadata                : User Meta data Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio n2 Name                        : TestHybirdConnection2 Type                        : Microsoft.Relay/HybridConnections</span></span>

### <span data-ttu-id="79198-154">Örnekler-2: Özellikler</span><span class="sxs-lookup"><span data-stu-id="79198-154">Examples - 2 : Properties</span></span>
<span data-ttu-id="79198-155">CreatedAt: 4/26/2017 10:04:15 PM UpdatedAt: 4/26/2017 10:04:15 PM ListenerCount: Requiresclientauthor,: TestHybirdConnection1 Type: Microsoft. Relay/HybridConnections</span><span class="sxs-lookup"><span data-stu-id="79198-155">CreatedAt                   : 4/26/2017 10:04:15 PM UpdatedAt                   : 4/26/2017 10:04:15 PM ListenerCount               : RequiresClientAuthorization : True UserMetadata                : User Meta data Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio n1 Name                        : TestHybirdConnection1 Type                        : Microsoft.Relay/HybridConnections</span></span>

## <span data-ttu-id="79198-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="79198-156">NOTES</span></span>

## <span data-ttu-id="79198-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="79198-157">RELATED LINKS</span></span>

