---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 7c766d3a112b880eaaa697e1f09d0d458dee5505
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763336"
---
# <span data-ttu-id="36d7a-101">Set-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="36d7a-101">Set-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="36d7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36d7a-102">SYNOPSIS</span></span>
<span data-ttu-id="36d7a-103">Belirtilen geçiş ad alanındaki bir HybridConnection açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="36d7a-103">Updates the description of a HybridConnection in the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36d7a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="36d7a-104">SYNTAX</span></span>

### <span data-ttu-id="36d7a-105">HybridConnectionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="36d7a-105">HybridConnectionInputObjectSet</span></span>
```
Set-AzureRmRelayHybridConnection -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-InputObject <HybridConnectionAttibutes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="36d7a-106">HybridConnectionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="36d7a-106">HybridConnectionPropertiesSet</span></span>
```
Set-AzureRmRelayHybridConnection -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36d7a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="36d7a-107">DESCRIPTION</span></span>
<span data-ttu-id="36d7a-108">Set-AzureRmRelayHybridConnection cmdlet 'i, belirtilen geçiş ad alanındaki HybridConnection öğesinin açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="36d7a-108">The Set-AzureRmRelayHybridConnection cmdlet updates the description for the HybridConnection in the specified Relay namespace.</span></span>

## <span data-ttu-id="36d7a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="36d7a-109">EXAMPLES</span></span>

### <span data-ttu-id="36d7a-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="36d7a-110">Example 1</span></span>
```
PS C:\>
PS C:\> $GetHybrid = Get-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
PS C:\> $GetHybrid.UserMetadata = "Test UserMetadata"
PS C:\> Set-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection -InputObject $GetHybrid
```

### <span data-ttu-id="36d7a-111">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="36d7a-111">Example 2</span></span>
```
PS C:\> Set-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection -UserMetadata = "Test UserMetadata updated"
```

<span data-ttu-id="36d7a-112">Belirtilen HybridConnection öğesini belirtilen ad alanındaki yeni bir açıklamayla güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="36d7a-112">Updates the specified HybridConnection with a new description in the specified namespace.</span></span>
<span data-ttu-id="36d7a-113">Bu örnek, yeni değeri olan UserMetadata özelliğini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="36d7a-113">This example updates the UserMetadata property with new value.</span></span>

## <span data-ttu-id="36d7a-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="36d7a-114">PARAMETERS</span></span>

### <span data-ttu-id="36d7a-115">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="36d7a-115">-UserMetadata</span></span>
<span data-ttu-id="36d7a-116">Kullanıcı tanımlı dize verilerinin HybridConnection uç noktasına depolanması için bir yer tutucudur. ekip listesi ve kişi bilgileri gibi açıklayıcı verileri depolamak için kullanılabilir, Kullanıcı tanımlı yapılandırma ayarları da depolanabilir.</span><span class="sxs-lookup"><span data-stu-id="36d7a-116">Gets or sets usermetadata is a placeholder to store user-defined string data for the HybridConnection endpoint.e.g. it can be used to store  descriptive data, such as list of teams and their contact information also user-defined configuration settings can be stored.</span></span>

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

### <span data-ttu-id="36d7a-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="36d7a-117">-Confirm</span></span>
<span data-ttu-id="36d7a-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="36d7a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36d7a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36d7a-119">-WhatIf</span></span>
<span data-ttu-id="36d7a-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="36d7a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36d7a-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="36d7a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36d7a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36d7a-122">-InputObject</span></span>
<span data-ttu-id="36d7a-123">HybridConnections nesnesi.</span><span class="sxs-lookup"><span data-stu-id="36d7a-123">HybridConnections object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes
Parameter Sets: HybridConnectionInputObjectSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36d7a-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="36d7a-124">-Name</span></span>
<span data-ttu-id="36d7a-125">HybridConnections adı.</span><span class="sxs-lookup"><span data-stu-id="36d7a-125">HybridConnections Name.</span></span>

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

### <span data-ttu-id="36d7a-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="36d7a-126">-Namespace</span></span>
<span data-ttu-id="36d7a-127">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="36d7a-127">Namespace Name.</span></span>

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

### <span data-ttu-id="36d7a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36d7a-128">-ResourceGroupName</span></span>
<span data-ttu-id="36d7a-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="36d7a-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="36d7a-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36d7a-130">-DefaultProfile</span></span>
<span data-ttu-id="36d7a-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="36d7a-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36d7a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36d7a-132">CommonParameters</span></span>
<span data-ttu-id="36d7a-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="36d7a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36d7a-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36d7a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36d7a-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="36d7a-135">INPUTS</span></span>

### <span data-ttu-id="36d7a-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36d7a-136">-ResourceGroupName</span></span>
<span data-ttu-id="36d7a-137">System. String</span><span class="sxs-lookup"><span data-stu-id="36d7a-137">System.String</span></span>

### <span data-ttu-id="36d7a-138">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="36d7a-138">-NamespaceName</span></span>
<span data-ttu-id="36d7a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="36d7a-139">System.String</span></span>

### <span data-ttu-id="36d7a-140">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="36d7a-140">-WcfRelayName</span></span>
<span data-ttu-id="36d7a-141">System. String</span><span class="sxs-lookup"><span data-stu-id="36d7a-141">System.String</span></span>

### <span data-ttu-id="36d7a-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36d7a-142">-InputObject</span></span>
<span data-ttu-id="36d7a-143">Microsoft. Azure. Commands. Relay. modeller. HybridConnectionAttibutes</span><span class="sxs-lookup"><span data-stu-id="36d7a-143">Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes</span></span>

### <span data-ttu-id="36d7a-144">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="36d7a-144">-UserMetadata</span></span>
<span data-ttu-id="36d7a-145">System. String</span><span class="sxs-lookup"><span data-stu-id="36d7a-145">System.String</span></span>

## <span data-ttu-id="36d7a-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="36d7a-146">OUTPUTS</span></span>

### <span data-ttu-id="36d7a-147">Örnekler-1: InputObject</span><span class="sxs-lookup"><span data-stu-id="36d7a-147">Examples - 1 : InputObject</span></span>
<span data-ttu-id="36d7a-148">CreatedAt: 4/26/2017 10:04:15 PM UpdatedAt: 4/26/2017 10:08:11 PM ListenerCount: Requiresclientauthorroa:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio N2 adı: TestHybirdConnection2 Type: Microsoft. Relay/HybridConnections</span><span class="sxs-lookup"><span data-stu-id="36d7a-148">CreatedAt                   : 4/26/2017 10:04:15 PM UpdatedAt                   : 4/26/2017 10:08:11 PM ListenerCount               : RequiresClientAuthorization : True UserMetadata                : Test UserMetadata Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio n2 Name                        : TestHybirdConnection2 Type                        : Microsoft.Relay/HybridConnections</span></span>

### <span data-ttu-id="36d7a-149">Örnekler-2: Özellikler</span><span class="sxs-lookup"><span data-stu-id="36d7a-149">Examples - 2 : Properties</span></span>
<span data-ttu-id="36d7a-150">CreatedAt: 4/26/2017 10:04:15 PM UpdatedAt: 4/26/2017 10:10:25 PM ListenerCount: Requiresclientauthorroa:/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio N1 adı: TestHybirdConnection1 Type: Microsoft. Relay/HybridConnections</span><span class="sxs-lookup"><span data-stu-id="36d7a-150">CreatedAt                   : 4/26/2017 10:04:15 PM UpdatedAt                   : 4/26/2017 10:10:25 PM ListenerCount               : RequiresClientAuthorization : True UserMetadata                : Test UserMetadata updated Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS /providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio n1 Name                        : TestHybirdConnection1 Type                        : Microsoft.Relay/HybridConnections</span></span>

## <span data-ttu-id="36d7a-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="36d7a-151">NOTES</span></span>

## <span data-ttu-id="36d7a-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="36d7a-152">RELATED LINKS</span></span>

