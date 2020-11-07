---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/new-azurermrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 9398c2229b31e432e55e5c4b11e72d3360b52fbe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762845"
---
# <span data-ttu-id="c255b-101">New-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="c255b-101">New-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="c255b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c255b-102">SYNOPSIS</span></span>
<span data-ttu-id="c255b-103">Belirtilen geçiş ad alanında HybridConnection oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c255b-103">Creates a HybridConnection in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c255b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c255b-104">SYNTAX</span></span>

### <span data-ttu-id="c255b-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c255b-105">HybridConnectionInputObjectSet</span></span>
```
New-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <HybridConnectionAttibutes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c255b-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="c255b-106">HybridConnectionPropertiesSet</span></span>
```
New-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RequiresClientAuthorization <Boolean>] [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c255b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c255b-107">DESCRIPTION</span></span>
<span data-ttu-id="c255b-108">New-AzureRmRelayHybridConnection cmdlet 'i belirtilen geçiş ad boşluğunda bir HybridConnection oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c255b-108">The New-AzureRmRelayHybridConnection cmdlet creates a HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="c255b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c255b-109">EXAMPLES</span></span>

### <span data-ttu-id="c255b-110">Örnek 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="c255b-110">Example 1 - InputObject</span></span>
```
PS C:\> $getHybirdConnection = Get-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-HybirdConnection -Name TestHybirdConnection1
PS C:\> $getHybirdConnection.UserMetadata = "TestHybirdConnection2"
PS C:\> $getHybirdConnection.RequiresClientAuthorization = $False
PS C:\> New-AzureRmRelayHybridConnection -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection2 -InputObject $getHybirdConnection

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

<span data-ttu-id="c255b-111">\` \` Belirtilen geçiş ad alanı \` TestNamespace-hybirvseçconnection 'Da yeni bir hybirvseçconnection TestHybirdConnection2 oluşturur \` .</span><span class="sxs-lookup"><span data-stu-id="c255b-111">Creates a new HybirdConnection \`TestHybirdConnection2\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

### <span data-ttu-id="c255b-112">Örnek 2-Özellikler</span><span class="sxs-lookup"><span data-stu-id="c255b-112">Example 2 - Properties</span></span>
```
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection1 -RequiresClientAuthorization $True -UserMetadata "User Meta data"

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

<span data-ttu-id="c255b-113">\` \` Belirtilen geçiş ad alanı \` TestNamespace-hybirvseçconnection 'Da yeni bir hybirvseçconnection TestHybirdConnection1 oluşturur \` .</span><span class="sxs-lookup"><span data-stu-id="c255b-113">Creates a new HybirdConnection \`TestHybirdConnection1\` in the specified Relay namespace \`TestNameSpace-HybirdConnection\`.</span></span>

## <span data-ttu-id="c255b-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c255b-114">PARAMETERS</span></span>

### <span data-ttu-id="c255b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c255b-115">-DefaultProfile</span></span>
<span data-ttu-id="c255b-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c255b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c255b-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c255b-117">-InputObject</span></span>
<span data-ttu-id="c255b-118">HybridConnections nesnesi.</span><span class="sxs-lookup"><span data-stu-id="c255b-118">HybridConnections object.</span></span>

```yaml
Type: HybridConnectionAttibutes
Parameter Sets: HybridConnectionInputObjectSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c255b-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="c255b-119">-Name</span></span>
<span data-ttu-id="c255b-120">HybridConnections adı.</span><span class="sxs-lookup"><span data-stu-id="c255b-120">HybridConnections Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c255b-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c255b-121">-Namespace</span></span>
<span data-ttu-id="c255b-122">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="c255b-122">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c255b-123">-Requiresclientauthorter</span><span class="sxs-lookup"><span data-stu-id="c255b-123">-RequiresClientAuthorization</span></span>
<span data-ttu-id="c255b-124">Bu HybridConnections için istemci yetkilendirmesi gerekliyse doğru; Aksi takdirde, false</span><span class="sxs-lookup"><span data-stu-id="c255b-124">true if client authorization is needed for this HybridConnections; otherwise, false</span></span>

```yaml
Type: Boolean
Parameter Sets: HybridConnectionPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c255b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c255b-125">-ResourceGroupName</span></span>
<span data-ttu-id="c255b-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="c255b-126">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c255b-127">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="c255b-127">-UserMetadata</span></span>
<span data-ttu-id="c255b-128">Kullanıcı tanımlı dize verilerinin HybridConnection uç noktasına depolanması için bir yer tutucudur. ekip listesi ve kişi bilgileri gibi açıklayıcı verileri depolamak için kullanılabilir, Kullanıcı tanımlı yapılandırma ayarları da depolanabilir.</span><span class="sxs-lookup"><span data-stu-id="c255b-128">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

```yaml
Type: String
Parameter Sets: HybridConnectionPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c255b-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="c255b-129">-Confirm</span></span>
<span data-ttu-id="c255b-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c255b-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c255b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c255b-131">-WhatIf</span></span>
<span data-ttu-id="c255b-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c255b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c255b-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c255b-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c255b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c255b-134">CommonParameters</span></span>
<span data-ttu-id="c255b-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c255b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c255b-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c255b-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c255b-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c255b-137">INPUTS</span></span>

### <span data-ttu-id="c255b-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c255b-138">-ResourceGroupName</span></span>
<span data-ttu-id="c255b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c255b-139">System.String</span></span>

### <span data-ttu-id="c255b-140">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="c255b-140">-NamespaceName</span></span>
<span data-ttu-id="c255b-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c255b-141">System.String</span></span>

### <span data-ttu-id="c255b-142">-HybridConnectionsName</span><span class="sxs-lookup"><span data-stu-id="c255b-142">-HybridConnectionsName</span></span>
<span data-ttu-id="c255b-143">System. String</span><span class="sxs-lookup"><span data-stu-id="c255b-143">System.String</span></span>

### <span data-ttu-id="c255b-144">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c255b-144">-InputObject</span></span>
<span data-ttu-id="c255b-145">Microsoft. Azure. Commands. Relay. modeller. HybridConnectionAttibutes</span><span class="sxs-lookup"><span data-stu-id="c255b-145">Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes</span></span>

### <span data-ttu-id="c255b-146">-Requiresclientauthorter</span><span class="sxs-lookup"><span data-stu-id="c255b-146">-RequiresClientAuthorization</span></span>
<span data-ttu-id="c255b-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c255b-147">System.Boolean</span></span>

### <span data-ttu-id="c255b-148">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="c255b-148">-UserMetadata</span></span>
<span data-ttu-id="c255b-149">System. String</span><span class="sxs-lookup"><span data-stu-id="c255b-149">System.String</span></span>

## <span data-ttu-id="c255b-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c255b-150">OUTPUTS</span></span>

### <span data-ttu-id="c255b-151">Microsoft. Azure. Commands. Relay. modeller. HybridConnectionAttibutes</span><span class="sxs-lookup"><span data-stu-id="c255b-151">Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes</span></span>

## <span data-ttu-id="c255b-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c255b-152">NOTES</span></span>

## <span data-ttu-id="c255b-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c255b-153">RELATED LINKS</span></span>

