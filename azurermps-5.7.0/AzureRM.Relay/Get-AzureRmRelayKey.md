---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayKey.md
ms.openlocfilehash: 897ecd66665091fd3be1f14b31c00549912a0af8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587452"
---
# <span data-ttu-id="b9c4a-101">Get-AzureRmRelayKey</span><span class="sxs-lookup"><span data-stu-id="b9c4a-101">Get-AzureRmRelayKey</span></span>

## <span data-ttu-id="b9c4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9c4a-102">SYNOPSIS</span></span>
<span data-ttu-id="b9c4a-103">Verilen geçiş varlıkları (Namespace/WcfRelay/HybridConnection) için birincil ve ikincil bağlantı dizelerini alır.</span><span class="sxs-lookup"><span data-stu-id="b9c4a-103">Gets the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9c4a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b9c4a-104">SYNTAX</span></span>

### <span data-ttu-id="b9c4a-105">NamespaceAuthorizationRuleSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b9c4a-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9c4a-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="b9c4a-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9c4a-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="b9c4a-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9c4a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b9c4a-108">DESCRIPTION</span></span>
<span data-ttu-id="b9c4a-109">**Get-AzureRmRelayKey** cmdlet 'ı verilen geçiş varlıkları (Namespace/WcfRelay/HybridConnection) için birincil ve ikincil bağlantı dizelerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="b9c4a-109">The **Get-AzureRmRelayKey** cmdlet returns the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="b9c4a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b9c4a-110">EXAMPLES</span></span>

### <span data-ttu-id="b9c4a-111">Örnek 1-ad alanı</span><span class="sxs-lookup"><span data-stu-id="b9c4a-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

### <span data-ttu-id="b9c4a-112">Örnek 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="b9c4a-112">Example 2 - WcfRelay</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1  -WcfRelay TestWCFRelay1 -Name AuthoRule1
```

### <span data-ttu-id="b9c4a-113">Örnek 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="b9c4a-113">Example 3 - HybridConnection</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="b9c4a-114">Belirtilen geçiş varlıklarına (Namespace/WcfRelay/HybridConnection) birincil ve ikincil bağlantı dizesi.</span><span class="sxs-lookup"><span data-stu-id="b9c4a-114">Primary and secondary connection string to the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="b9c4a-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b9c4a-115">PARAMETERS</span></span>

### <span data-ttu-id="b9c4a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9c4a-116">-DefaultProfile</span></span>
<span data-ttu-id="b9c4a-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b9c4a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9c4a-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="b9c4a-118">-HybridConnection</span></span>
<span data-ttu-id="b9c4a-119">HybridConnection adı.</span><span class="sxs-lookup"><span data-stu-id="b9c4a-119">HybridConnection Name.</span></span>

```yaml
Type: String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9c4a-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="b9c4a-120">-Name</span></span>
<span data-ttu-id="b9c4a-121">AuthorizationRule adı.</span><span class="sxs-lookup"><span data-stu-id="b9c4a-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="b9c4a-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b9c4a-122">-Namespace</span></span>
<span data-ttu-id="b9c4a-123">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="b9c4a-123">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9c4a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9c4a-124">-ResourceGroupName</span></span>
<span data-ttu-id="b9c4a-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b9c4a-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="b9c4a-126">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="b9c4a-126">-WcfRelay</span></span>
<span data-ttu-id="b9c4a-127">WcfRelay adı.</span><span class="sxs-lookup"><span data-stu-id="b9c4a-127">WcfRelay Name.</span></span>

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9c4a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9c4a-128">CommonParameters</span></span>
<span data-ttu-id="b9c4a-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b9c4a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9c4a-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9c4a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9c4a-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b9c4a-131">INPUTS</span></span>

### <span data-ttu-id="b9c4a-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9c4a-132">-ResourceGroupName</span></span>
 <span data-ttu-id="b9c4a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b9c4a-133">System.String</span></span> 

### <span data-ttu-id="b9c4a-134">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="b9c4a-134">-NamespaceName</span></span>
 <span data-ttu-id="b9c4a-135">System. String</span><span class="sxs-lookup"><span data-stu-id="b9c4a-135">System.String</span></span> 
 

### <span data-ttu-id="b9c4a-136">-HybridConnectionsName</span><span class="sxs-lookup"><span data-stu-id="b9c4a-136">-HybridConnectionsName</span></span>
 <span data-ttu-id="b9c4a-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b9c4a-137">System.String</span></span> 

### <span data-ttu-id="b9c4a-138">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="b9c4a-138">-WcfRelayName</span></span>
 <span data-ttu-id="b9c4a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b9c4a-139">System.String</span></span> 

### <span data-ttu-id="b9c4a-140">-Ad</span><span class="sxs-lookup"><span data-stu-id="b9c4a-140">-Name</span></span>
 <span data-ttu-id="b9c4a-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b9c4a-141">System.String</span></span>

## <span data-ttu-id="b9c4a-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b9c4a-142">OUTPUTS</span></span>

### <span data-ttu-id="b9c4a-143">Microsoft. Azure. Commands. Relay. modeller. AuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="b9c4a-143">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleKeysAttributes</span></span>

### <span data-ttu-id="b9c4a-144">Örnek 1-ad alanı</span><span class="sxs-lookup"><span data-stu-id="b9c4a-144">Example 1 - Namespace</span></span>
<span data-ttu-id="b9c4a-145">PrimaryConnectionString: Endpoint = SB://TestNamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #</span><span class="sxs-lookup"><span data-stu-id="b9c4a-145">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="b9c4a-146">Örnek 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="b9c4a-146">Example 2 - WcfRelay</span></span>
<span data-ttu-id="b9c4a-147">PrimaryConnectionString: Endpoint = SB://TestNamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #; EntityPath = TestWCFRelay1 SecondaryConnectionString: Endpoint = SB://TestNamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #; EntityPath = TestWCFRelay1 PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #</span><span class="sxs-lookup"><span data-stu-id="b9c4a-147">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="b9c4a-148">Örnek 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="b9c4a-148">Example 3 - HybridConnection</span></span>
<span data-ttu-id="b9c4a-149">PrimaryConnectionString: Endpoint = SB://TestNamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #; EntityPath = TestHybridConnection SecondaryConnectionString: Endpoint = SB://TestNamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #; EntityPath = TestHybridConnection PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #</span><span class="sxs-lookup"><span data-stu-id="b9c4a-149">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

## <span data-ttu-id="b9c4a-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b9c4a-150">NOTES</span></span>

## <span data-ttu-id="b9c4a-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b9c4a-151">RELATED LINKS</span></span>

