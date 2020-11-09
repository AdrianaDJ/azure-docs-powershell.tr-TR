---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzWcfRelay.md
ms.openlocfilehash: 8fa9f3e2bbded846569609d9b1bae191d9f5ad89
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324430"
---
# <span data-ttu-id="d34ea-101">New-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="d34ea-101">New-AzWcfRelay</span></span>

## <span data-ttu-id="d34ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d34ea-102">SYNOPSIS</span></span>
<span data-ttu-id="d34ea-103">Belirtilen geçiş ad alanında WcfRelay oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d34ea-103">Creates a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="d34ea-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d34ea-104">SYNTAX</span></span>

### <span data-ttu-id="d34ea-105">WcfRelayInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d34ea-105">WcfRelayInputObjectSet</span></span>
```
New-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSWcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d34ea-106">WcfRelayPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="d34ea-106">WcfRelayPropertiesSet</span></span>
```
New-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-WcfRelayType <String>]
 [-RequiresClientAuthorization <Boolean>] [-RequiresTransportSecurity <Boolean>] [-UserMetadata <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d34ea-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d34ea-107">DESCRIPTION</span></span>
<span data-ttu-id="d34ea-108">New-AzWcfRelay cmdlet 'i belirtilen geçiş ad alanında WcfRelay oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d34ea-108">The New-AzWcfRelay cmdlet creates a WcfRelay in the specified Relay namespace.</span></span>

## <span data-ttu-id="d34ea-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d34ea-109">EXAMPLES</span></span>

### <span data-ttu-id="d34ea-110">Örnek 1-InputObject</span><span class="sxs-lookup"><span data-stu-id="d34ea-110">Example 1 - InputObject</span></span>
```
PS C:\> $getWcfRelay = Get-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay1
PS C:\> $GetWcfRelay.UserMetadata = "TestWCFRelay2"
PS C:\> $GetWcfRelay.RequiresClientAuthorization = $False
PS C:\> $GetWcfRelay.RelayType = "Http"
PS C:\> New-AzWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay2 -InputObject

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

<span data-ttu-id="d34ea-111">\` \` Belirtilen geçiş ad alanı \` TestNamespace-Relay Içinde Yeni bir wcfrelay TestWCFRelay2 oluşturur \` .</span><span class="sxs-lookup"><span data-stu-id="d34ea-111">Creates a new WcfRelay \`TestWCFRelay2\` in the specified Relay namespace \`TestNameSpace-Relay\`.</span></span>

### <span data-ttu-id="d34ea-112">Örnek 2-Özellikler</span><span class="sxs-lookup"><span data-stu-id="d34ea-112">Example 2 - Properties</span></span>
```
PS C:\> New-AzWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay -WcfRelayType "NetTcp"  -RequiresClientAuthorization $True -RequiresTransportSecurity $True -UserMetadata "User Meta data"

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

<span data-ttu-id="d34ea-113">\` \` Belirtilen geçiş ad alanı testwcfrelay-Relay1 için yeni bir wcfrelay testwcfrelay oluşturur \` \` .</span><span class="sxs-lookup"><span data-stu-id="d34ea-113">Creates a new WcfRelay \`TestWCFRelay\` in the specified Relay namespace \`TestNameSpace-Relay1\`.</span></span>

## <span data-ttu-id="d34ea-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d34ea-114">PARAMETERS</span></span>

### <span data-ttu-id="d34ea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d34ea-115">-DefaultProfile</span></span>
<span data-ttu-id="d34ea-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d34ea-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d34ea-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d34ea-117">-InputObject</span></span>
<span data-ttu-id="d34ea-118">WcfRelay nesnesi.</span><span class="sxs-lookup"><span data-stu-id="d34ea-118">WcfRelay object.</span></span>

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

### <span data-ttu-id="d34ea-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="d34ea-119">-Name</span></span>
<span data-ttu-id="d34ea-120">WcfRelay adı.</span><span class="sxs-lookup"><span data-stu-id="d34ea-120">WcfRelay Name.</span></span>

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

### <span data-ttu-id="d34ea-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d34ea-121">-Namespace</span></span>
<span data-ttu-id="d34ea-122">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="d34ea-122">Namespace Name.</span></span>

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

### <span data-ttu-id="d34ea-123">-Requiresclientauthorter</span><span class="sxs-lookup"><span data-stu-id="d34ea-123">-RequiresClientAuthorization</span></span>
<span data-ttu-id="d34ea-124">Bu geçiş için istemci yetkilendirmesi gerekliyse doğru; Aksi takdirde, false</span><span class="sxs-lookup"><span data-stu-id="d34ea-124">true if client authorization is needed for this relay; otherwise, false</span></span>

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

### <span data-ttu-id="d34ea-125">-RequiresTransportSecurity</span><span class="sxs-lookup"><span data-stu-id="d34ea-125">-RequiresTransportSecurity</span></span>
<span data-ttu-id="d34ea-126">Bu geçiş için taşıma güvenliği gerekliyse doğru; Aksi takdirde, false</span><span class="sxs-lookup"><span data-stu-id="d34ea-126">true if transport security is needed for this relay; otherwise, false</span></span>

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

### <span data-ttu-id="d34ea-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d34ea-127">-ResourceGroupName</span></span>
<span data-ttu-id="d34ea-128">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="d34ea-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="d34ea-129">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="d34ea-129">-UserMetadata</span></span>
<span data-ttu-id="d34ea-130">Kullanıcı tanımlı dize verilerinin HybridConnection uç noktasına depolanması için bir yer tutucudur. ekip listesi ve kişi bilgileri gibi açıklayıcı verileri depolamak için kullanılabilir, Kullanıcı tanımlı yapılandırma ayarları da depolanabilir.</span><span class="sxs-lookup"><span data-stu-id="d34ea-130">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="d34ea-131">-WcfRelayType</span><span class="sxs-lookup"><span data-stu-id="d34ea-131">-WcfRelayType</span></span>
<span data-ttu-id="d34ea-132">WcfRelay türü.</span><span class="sxs-lookup"><span data-stu-id="d34ea-132">WcfRelay Type.</span></span>
<span data-ttu-id="d34ea-133">Olası değerler: ' NetTcp ' veya ' http '</span><span class="sxs-lookup"><span data-stu-id="d34ea-133">Possible values include: 'NetTcp' or 'Http'</span></span>

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

### <span data-ttu-id="d34ea-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="d34ea-134">-Confirm</span></span>
<span data-ttu-id="d34ea-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d34ea-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d34ea-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d34ea-136">-WhatIf</span></span>
<span data-ttu-id="d34ea-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d34ea-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d34ea-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d34ea-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d34ea-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d34ea-139">CommonParameters</span></span>
<span data-ttu-id="d34ea-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d34ea-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d34ea-141">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d34ea-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d34ea-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d34ea-142">INPUTS</span></span>

### <span data-ttu-id="d34ea-143">System. String</span><span class="sxs-lookup"><span data-stu-id="d34ea-143">System.String</span></span>

### <span data-ttu-id="d34ea-144">Microsoft. Azure. Commands. Relay. modeller. PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="d34ea-144">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

### <span data-ttu-id="d34ea-145">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="d34ea-145">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="d34ea-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d34ea-146">OUTPUTS</span></span>

### <span data-ttu-id="d34ea-147">Microsoft. Azure. Commands. Relay. modeller. PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="d34ea-147">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="d34ea-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d34ea-148">NOTES</span></span>

## <span data-ttu-id="d34ea-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d34ea-149">RELATED LINKS</span></span>
