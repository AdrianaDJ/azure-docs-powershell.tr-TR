---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/new-azurermwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmWcfRelay.md
ms.openlocfilehash: 3aa57c1ec70d560a0fee395b27d79372bdf4fd61
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587177"
---
# <span data-ttu-id="67e2f-101">New-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="67e2f-101">New-AzureRmWcfRelay</span></span>

## <span data-ttu-id="67e2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67e2f-102">SYNOPSIS</span></span>
<span data-ttu-id="67e2f-103">Belirtilen geçiş ad alanında WcfRelay oluşturur.</span><span class="sxs-lookup"><span data-stu-id="67e2f-103">Creates a WcfRelay in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67e2f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="67e2f-104">SYNTAX</span></span>

### <span data-ttu-id="67e2f-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="67e2f-105">WcfRelayInputObjectSet</span></span>
```
New-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <WcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="67e2f-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="67e2f-106">WcfRelayPropertiesSet</span></span>
```
New-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-WcfRelayType <String>] [-RequiresClientAuthorization <Boolean>] [-RequiresTransportSecurity <Boolean>]
 [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67e2f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="67e2f-107">DESCRIPTION</span></span>
<span data-ttu-id="67e2f-108">New-AzureRmWcfRelay cmdlet 'i belirtilen geçiş ad alanında WcfRelay oluşturur.</span><span class="sxs-lookup"><span data-stu-id="67e2f-108">The New-AzureRmWcfRelay cmdlet creates a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="67e2f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="67e2f-109">EXAMPLES</span></span>

### <span data-ttu-id="67e2f-110">Örnek 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="67e2f-110">Example 1 - InputObject</span></span>
```
PS C:\> $getWcfRelay = Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay1
PS C:\> $GetWcfRelay.UserMetadata = "TestWCFRelay2"
PS C:\> $GetWcfRelay.RequiresClientAuthorization = $False
PS C:\> $GetWcfRelay.RelayType = "Http"
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay2 -InputObject

RelayType                   : Http
CreatedAt                   : 4/26/2017 5:14:46 PM
UpdatedAt                   : 4/26/2017 5:14:46 PM
ListenerCount               :
RequiresClientAuthorization : False
RequiresTransportSecurity   : True
IsDynamic                   : False
UserMetadata                : TestWCFRelay2
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel
                              ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2
Name                        : TestWCFRelay2
Type                        : Microsoft.Relay/WcfRelays
```

<span data-ttu-id="67e2f-111">\` \` Belirtilen geçiş ad alanı \` TestNamespace-Relay Içinde Yeni bir wcfrelay TestWCFRelay2 oluşturur \` .</span><span class="sxs-lookup"><span data-stu-id="67e2f-111">Creates a new WcfRelay \`TestWCFRelay2\` in the specified Relay namespace \`TestNameSpace-Relay\`.</span></span>

### <span data-ttu-id="67e2f-112">Örnek 2-Özellikler</span><span class="sxs-lookup"><span data-stu-id="67e2f-112">Example 2 - Properties</span></span>
```
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay -WcfRelayType "NetTcp"  -RequiresClientAuthorization $True -RequiresTransportSecurity $True -UserMetadata "User Meta data"

RelayType                   : NetTcp
CreatedAt                   : 4/26/2017 5:20:08 PM
UpdatedAt                   : 4/26/2017 5:20:08 PM
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

<span data-ttu-id="67e2f-113">\` \` Belirtilen geçiş ad alanı testwcfrelay-Relay1 için yeni bir wcfrelay testwcfrelay oluşturur \` \` .</span><span class="sxs-lookup"><span data-stu-id="67e2f-113">Creates a new WcfRelay \`TestWCFRelay\` in the specified Relay namespace \`TestNameSpace-Relay1\`.</span></span>

## <span data-ttu-id="67e2f-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="67e2f-114">PARAMETERS</span></span>

### <span data-ttu-id="67e2f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67e2f-115">-DefaultProfile</span></span>
<span data-ttu-id="67e2f-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="67e2f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67e2f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67e2f-117">-InputObject</span></span>
<span data-ttu-id="67e2f-118">WcfRelay nesnesi.</span><span class="sxs-lookup"><span data-stu-id="67e2f-118">WcfRelay object.</span></span>

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

### <span data-ttu-id="67e2f-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="67e2f-119">-Name</span></span>
<span data-ttu-id="67e2f-120">WcfRelay adı.</span><span class="sxs-lookup"><span data-stu-id="67e2f-120">WcfRelay Name.</span></span>

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

### <span data-ttu-id="67e2f-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="67e2f-121">-Namespace</span></span>
<span data-ttu-id="67e2f-122">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="67e2f-122">Namespace Name.</span></span>

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

### <span data-ttu-id="67e2f-123">-Requiresclientauthorter</span><span class="sxs-lookup"><span data-stu-id="67e2f-123">-RequiresClientAuthorization</span></span>
<span data-ttu-id="67e2f-124">Bu geçiş için istemci yetkilendirmesi gerekliyse doğru; Aksi takdirde, false</span><span class="sxs-lookup"><span data-stu-id="67e2f-124">true if client authorization is needed for this relay; otherwise, false</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: WcfRelayPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67e2f-125">-RequiresTransportSecurity</span><span class="sxs-lookup"><span data-stu-id="67e2f-125">-RequiresTransportSecurity</span></span>
<span data-ttu-id="67e2f-126">Bu geçiş için taşıma güvenliği gerekliyse doğru; Aksi takdirde, false</span><span class="sxs-lookup"><span data-stu-id="67e2f-126">true if transport security is needed for this relay; otherwise, false</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: WcfRelayPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67e2f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67e2f-127">-ResourceGroupName</span></span>
<span data-ttu-id="67e2f-128">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="67e2f-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="67e2f-129">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="67e2f-129">-UserMetadata</span></span>
<span data-ttu-id="67e2f-130">Kullanıcı tanımlı dize verilerinin HybridConnection uç noktasına depolanması için bir yer tutucudur. ekip listesi ve kişi bilgileri gibi açıklayıcı verileri depolamak için kullanılabilir, Kullanıcı tanımlı yapılandırma ayarları da depolanabilir.</span><span class="sxs-lookup"><span data-stu-id="67e2f-130">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="67e2f-131">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="67e2f-131">-WcfRelayType</span></span>
<span data-ttu-id="67e2f-132">WcfRelay türü.</span><span class="sxs-lookup"><span data-stu-id="67e2f-132">WcfRelay Type.</span></span>
<span data-ttu-id="67e2f-133">Olası değerler: ' NetTcp ' veya ' http '</span><span class="sxs-lookup"><span data-stu-id="67e2f-133">Possible values include: 'NetTcp' or 'Http'</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayPropertiesSet
Aliases:
Accepted values: NetTcp, Http

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67e2f-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="67e2f-134">-Confirm</span></span>
<span data-ttu-id="67e2f-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="67e2f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67e2f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67e2f-136">-WhatIf</span></span>
<span data-ttu-id="67e2f-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="67e2f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67e2f-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="67e2f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67e2f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67e2f-139">CommonParameters</span></span>
<span data-ttu-id="67e2f-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="67e2f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="67e2f-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67e2f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67e2f-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="67e2f-142">INPUTS</span></span>

### <span data-ttu-id="67e2f-143">System. String</span><span class="sxs-lookup"><span data-stu-id="67e2f-143">System.String</span></span>
<span data-ttu-id="67e2f-144">Microsoft. Azure. Commands. Relay. modeller. PSWcfRelayAttributes System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="67e2f-144">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>


## <span data-ttu-id="67e2f-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="67e2f-145">OUTPUTS</span></span>

### <span data-ttu-id="67e2f-146">Microsoft. Azure. Commands. Relay. modeller. PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="67e2f-146">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>


## <span data-ttu-id="67e2f-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="67e2f-147">NOTES</span></span>

## <span data-ttu-id="67e2f-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="67e2f-148">RELATED LINKS</span></span>
