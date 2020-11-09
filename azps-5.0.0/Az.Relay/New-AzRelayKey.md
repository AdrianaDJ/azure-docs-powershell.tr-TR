---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayKey.md
ms.openlocfilehash: f475d3f661d1bd1696d9ae728998bb609222816d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324439"
---
# <span data-ttu-id="50237-101">New-AzRelayKey</span><span class="sxs-lookup"><span data-stu-id="50237-101">New-AzRelayKey</span></span>

## <span data-ttu-id="50237-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50237-102">SYNOPSIS</span></span>
<span data-ttu-id="50237-103">Verilen geçiş varlıkları (Namespace/WcfRelay/HybridConnection) için birincil veya ikincil bağlantı dizelerini yeniden oluşturur</span><span class="sxs-lookup"><span data-stu-id="50237-103">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection)</span></span>

## <span data-ttu-id="50237-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="50237-104">SYNTAX</span></span>

### <span data-ttu-id="50237-105">NamespaceAuthorizationRuleSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="50237-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> -RegenerateKey <String>
 [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50237-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="50237-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="50237-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="50237-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50237-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="50237-108">DESCRIPTION</span></span>
<span data-ttu-id="50237-109">**New-AzRelayKey** cmdlet 'ı verilen geçiş varlıkları (Namespace/WcfRelay/HybridConnection) için birincil ve ikincil bağlantı dizelerini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="50237-109">The **New-AzRelayKey** cmdlet generates the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="50237-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="50237-110">EXAMPLES</span></span>

### <span data-ttu-id="50237-111">Örnek 1-ad alanı</span><span class="sxs-lookup"><span data-stu-id="50237-111">Example 1 - Namespace</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="50237-112">Verilen Relay-Namespace varlığının birincil veya ikincil bağlantı dizelerini yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="50237-112">Regenerates the primary or secondary connection strings for the given Relay-Namespace entity.</span></span>

### <span data-ttu-id="50237-113">Örnek 1,1-sağlanan ad alanı KeyValue</span><span class="sxs-lookup"><span data-stu-id="50237-113">Example 1.1 - Namespace  KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey -KeyValue ###############

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey -KeyValue ###############

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="50237-114">verilen Relay-Namespace varlık için sağlanan anahtar değeri ile birincil veya ikincil bağlantı dizelerini oluşturur</span><span class="sxs-lookup"><span data-stu-id="50237-114">generates the primary or secondary connection strings for the given Relay-Namespace entity with Key Value Provided</span></span>

### <span data-ttu-id="50237-115">Örnek 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="50237-115">Example 2 - WcfRelay</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="50237-116">Verilen Relay-WcfRelay varlığının birincil veya ikincil bağlantı dizelerini yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="50237-116">Regenerates the primary or secondary connection strings for the given Relay-WcfRelay entity.</span></span>

### <span data-ttu-id="50237-117">Örnek 2,1-WcfRelay KeyValue sağlandı</span><span class="sxs-lookup"><span data-stu-id="50237-117">Example 2.1 - WcfRelay  KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey -KeyValue ############### 

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey -KeyValue ############### 

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="50237-118">verilen Relay-WcfRelay varlık için sağlanan anahtar değeri ile birincil veya ikincil bağlantı dizelerini oluşturur</span><span class="sxs-lookup"><span data-stu-id="50237-118">generates the primary or secondary connection strings for the given Relay-WcfRelay entity with Key Value Provided</span></span>

### <span data-ttu-id="50237-119">Örnek 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="50237-119">Example 3 - HybridConnection</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="50237-120">Verilen geçiş varlıkları (Namespace/WcfRelay/HybridConnection) için birincil veya ikincil bağlantı dizelerini yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="50237-120">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

### <span data-ttu-id="50237-121">Örnek 3,1-HybridConnection KeyValue sağlandı</span><span class="sxs-lookup"><span data-stu-id="50237-121">Example 3.1 - HybridConnection KeyValue Provided</span></span>
```
PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey -KeyValue ############### 

PS C:\> New-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey -KeyValue ############### 

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="50237-122">verilen Relay-HybridConnection varlık için sağlanan anahtar değeri ile birincil veya ikincil bağlantı dizelerini oluşturur</span><span class="sxs-lookup"><span data-stu-id="50237-122">generates the primary or secondary connection strings for the given Relay-HybridConnection entity with Key Value Provided</span></span>

## <span data-ttu-id="50237-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="50237-123">PARAMETERS</span></span>

### <span data-ttu-id="50237-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50237-124">-DefaultProfile</span></span>
<span data-ttu-id="50237-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="50237-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50237-126">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="50237-126">-HybridConnection</span></span>
<span data-ttu-id="50237-127">HybridConnection adı.</span><span class="sxs-lookup"><span data-stu-id="50237-127">HybridConnection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50237-128">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="50237-128">-KeyValue</span></span>
<span data-ttu-id="50237-129">SAS belirtecini imzalamak ve doğrulamak için Base64 ile kodlanmış 256 bit anahtar.</span><span class="sxs-lookup"><span data-stu-id="50237-129">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50237-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="50237-130">-Name</span></span>
<span data-ttu-id="50237-131">AuthorizationRule adı.</span><span class="sxs-lookup"><span data-stu-id="50237-131">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="50237-132">-Namespace</span><span class="sxs-lookup"><span data-stu-id="50237-132">-Namespace</span></span>
<span data-ttu-id="50237-133">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="50237-133">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50237-134">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="50237-134">-RegenerateKey</span></span>
<span data-ttu-id="50237-135">Anahtarları yeniden üret-' PrimaryKey '/' SecondaryKey '.</span><span class="sxs-lookup"><span data-stu-id="50237-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50237-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50237-136">-ResourceGroupName</span></span>
<span data-ttu-id="50237-137">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="50237-137">Resource Group Name.</span></span>

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

### <span data-ttu-id="50237-138">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="50237-138">-WcfRelay</span></span>
<span data-ttu-id="50237-139">WcfRelay adı.</span><span class="sxs-lookup"><span data-stu-id="50237-139">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50237-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="50237-140">-Confirm</span></span>
<span data-ttu-id="50237-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="50237-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50237-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50237-142">-WhatIf</span></span>
<span data-ttu-id="50237-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="50237-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50237-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="50237-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50237-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50237-145">CommonParameters</span></span>
<span data-ttu-id="50237-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="50237-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50237-147">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50237-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50237-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="50237-148">INPUTS</span></span>

### <span data-ttu-id="50237-149">System. String</span><span class="sxs-lookup"><span data-stu-id="50237-149">System.String</span></span>

## <span data-ttu-id="50237-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="50237-150">OUTPUTS</span></span>

### <span data-ttu-id="50237-151">Microsoft. Azure. Commands. Relay. modeller. PSAuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="50237-151">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span></span>

## <span data-ttu-id="50237-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="50237-152">NOTES</span></span>

## <span data-ttu-id="50237-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="50237-153">RELATED LINKS</span></span>
