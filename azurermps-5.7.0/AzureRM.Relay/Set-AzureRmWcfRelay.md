---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/set-azurermwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmWcfRelay.md
ms.openlocfilehash: 16df81633d4265b7b52dd2678bb58c80d4a756e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588805"
---
# <span data-ttu-id="b50bc-101">Set-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="b50bc-101">Set-AzureRmWcfRelay</span></span>

## <span data-ttu-id="b50bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b50bc-102">SYNOPSIS</span></span>
<span data-ttu-id="b50bc-103">Belirtilen geçiş ad alanındaki WcfRelay 'in açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b50bc-103">Updates the description of a WcfRelay in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b50bc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b50bc-104">SYNTAX</span></span>

### <span data-ttu-id="b50bc-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b50bc-105">WcfRelayInputObjectSet</span></span>
```
Set-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <WcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b50bc-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="b50bc-106">WcfRelayPropertiesSet</span></span>
```
Set-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b50bc-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b50bc-107">DESCRIPTION</span></span>
<span data-ttu-id="b50bc-108">Set-AzureRmWcfRelay cmdlet 'i belirtilen geçiş ad alanındaki WcfRelay 'in açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b50bc-108">The Set-AzureRmWcfRelay cmdlet updates the description for the WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="b50bc-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b50bc-109">EXAMPLES</span></span>

### <span data-ttu-id="b50bc-110">Örnek 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="b50bc-110">Example 1 - InputObject</span></span>
```
PS C:\>
PS C:\> $getWcfRelay = Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay
PS C:\> $getWcfRelay.UserMetadata = "usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc
riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored."
PS C:\> Set-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -InputObject $getWcfRelay
```

### <span data-ttu-id="b50bc-111">Örnek 2-Özellikler</span><span class="sxs-lookup"><span data-stu-id="b50bc-111">Example 2 - Properties</span></span>
```
PS C:\> Set-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1 -UserMetadata "User Meta data"
```

<span data-ttu-id="b50bc-112">Belirtilen WcfRelay 'i belirtilen ad alanındaki yeni bir açıklamayla güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b50bc-112">Updates the specified WcfRelay with a new description in the specified namespace.</span></span>
<span data-ttu-id="b50bc-113">Bu örnek, yeni değeri olan UserMetadata özelliğini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b50bc-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="b50bc-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b50bc-114">PARAMETERS</span></span>

### <span data-ttu-id="b50bc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b50bc-115">-DefaultProfile</span></span>
<span data-ttu-id="b50bc-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b50bc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b50bc-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b50bc-117">-InputObject</span></span>
<span data-ttu-id="b50bc-118">WcfRelay nesnesi.</span><span class="sxs-lookup"><span data-stu-id="b50bc-118">WcfRelay object.</span></span>

```yaml
Type: WcfRelayAttributes
Parameter Sets: WcfRelayInputObjectSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b50bc-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="b50bc-119">-Name</span></span>
<span data-ttu-id="b50bc-120">WcfRelay adı.</span><span class="sxs-lookup"><span data-stu-id="b50bc-120">WcfRelay Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b50bc-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b50bc-121">-Namespace</span></span>
<span data-ttu-id="b50bc-122">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="b50bc-122">Namespace Name.</span></span>

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

### <span data-ttu-id="b50bc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b50bc-123">-ResourceGroupName</span></span>
<span data-ttu-id="b50bc-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b50bc-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="b50bc-125">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="b50bc-125">-UserMetadata</span></span>
<span data-ttu-id="b50bc-126">Kullanıcı tanımlı dize verilerinin HybridConnection uç noktasına depolanması için bir yer tutucudur. ekip listesi ve kişi bilgileri gibi açıklayıcı verileri depolamak için kullanılabilir, Kullanıcı tanımlı yapılandırma ayarları da depolanabilir.</span><span class="sxs-lookup"><span data-stu-id="b50bc-126">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

```yaml
Type: String
Parameter Sets: WcfRelayPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b50bc-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="b50bc-127">-Confirm</span></span>
<span data-ttu-id="b50bc-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b50bc-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b50bc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b50bc-129">-WhatIf</span></span>
<span data-ttu-id="b50bc-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b50bc-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b50bc-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b50bc-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b50bc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b50bc-132">CommonParameters</span></span>
<span data-ttu-id="b50bc-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b50bc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b50bc-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b50bc-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b50bc-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b50bc-135">INPUTS</span></span>

### <span data-ttu-id="b50bc-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b50bc-136">-ResourceGroupName</span></span>
<span data-ttu-id="b50bc-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b50bc-137">System.String</span></span>

### <span data-ttu-id="b50bc-138">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="b50bc-138">-NamespaceName</span></span>
<span data-ttu-id="b50bc-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b50bc-139">System.String</span></span>

### <span data-ttu-id="b50bc-140">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="b50bc-140">-WcfRelayName</span></span>
<span data-ttu-id="b50bc-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b50bc-141">System.String</span></span>

### <span data-ttu-id="b50bc-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b50bc-142">-InputObject</span></span>
<span data-ttu-id="b50bc-143">Microsoft. Azure. Commands. Relay. modeller. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="b50bc-143">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>

### <span data-ttu-id="b50bc-144">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="b50bc-144">-WcfRelayType</span></span>
<span data-ttu-id="b50bc-145">System. String</span><span class="sxs-lookup"><span data-stu-id="b50bc-145">System.String</span></span>

### <span data-ttu-id="b50bc-146">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="b50bc-146">-UserMetadata</span></span>
<span data-ttu-id="b50bc-147">System. String</span><span class="sxs-lookup"><span data-stu-id="b50bc-147">System.String</span></span>

## <span data-ttu-id="b50bc-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b50bc-148">OUTPUTS</span></span>

### <span data-ttu-id="b50bc-149">Microsoft. Azure. Commands. Relay. modeller. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="b50bc-149">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>

### <span data-ttu-id="b50bc-150">Örnek 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="b50bc-150">Example 1 - InputObject</span></span>

### <span data-ttu-id="b50bc-151">Microsoft. Azure. Commands. Relay. modeller. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="b50bc-151">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>
<span data-ttu-id="b50bc-152">RelayType: http CreatedAt: 4/26/2017 5:14:46 PM UpdatedAt: 4/26/2017 5:16:50 PM ListenerCount: Requiresclientauthoryet: false Requirestransportsecurıty: doğru IsDynamic: false UserMetadata: usermetadata, HybridConnection uç noktası için Kullanıcı tanımlı dize verilerini depolamak için yer tutucudur. ekip listesi ve kişi bilgileri gibi DESC riptive verilerini depolamak için kullanılabilir, Kullanıcı tanımlı yapılandırma ayarları da depolanabilir.</span><span class="sxs-lookup"><span data-stu-id="b50bc-152">RelayType                   : Http CreatedAt                   : 4/26/2017 5:14:46 PM UpdatedAt                   : 4/26/2017 5:16:50 PM ListenerCount               : RequiresClientAuthorization : False RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  desc riptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>
<span data-ttu-id="b50bc-153">ID:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/ad uzayları/TestNameSpace-Relay1/Wcfretakları/TestWCFRelay2 adı: TestWCFRelay2 tür: Microsoft. Relay/Wcfreş</span><span class="sxs-lookup"><span data-stu-id="b50bc-153">Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2 Name                        : TestWCFRelay2 Type                        : Microsoft.Relay/WcfRelays</span></span>

### <span data-ttu-id="b50bc-154">Örnek 2-Özellikler</span><span class="sxs-lookup"><span data-stu-id="b50bc-154">Example 2 - Properties</span></span>

### <span data-ttu-id="b50bc-155">Microsoft. Azure. Commands. Relay. modeller. WcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="b50bc-155">Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes</span></span>
<span data-ttu-id="b50bc-156">RelayType: NetTcp createdat: 4/26/2017 5:20:08 PM updatedat: 4/26/2017 5:26:09 PM listenercount: requiresclientauthorleme: doğru requirestransportsecurıty: true IsDynamic: false usermetadata: Kullanıcı meta veri kimliği:/Subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/default-Storage-WestUS/Providers/Microsoft.rel ay/namespaces/TestNamespace-Relay1/wcfre,/testwcfrelay Name: testwcfrelay Type: Microsoft. Relay/wcfreroa</span><span class="sxs-lookup"><span data-stu-id="b50bc-156">RelayType                   : NetTcp CreatedAt                   : 4/26/2017 5:20:08 PM UpdatedAt                   : 4/26/2017 5:26:09 PM ListenerCount               : RequiresClientAuthorization : True RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : User Meta data Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay Name                        : TestWCFRelay Type                        : Microsoft.Relay/WcfRelays</span></span>

## <span data-ttu-id="b50bc-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b50bc-157">NOTES</span></span>

## <span data-ttu-id="b50bc-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b50bc-158">RELATED LINKS</span></span>

