---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayKey.md
ms.openlocfilehash: 4434802f1025e24bb249ee503ed2267e9187a2c2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938170"
---
# <span data-ttu-id="57430-101">Get-AzRelayKey</span><span class="sxs-lookup"><span data-stu-id="57430-101">Get-AzRelayKey</span></span>

## <span data-ttu-id="57430-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57430-102">SYNOPSIS</span></span>
<span data-ttu-id="57430-103">Verilen geçiş varlıkları (Namespace/WcfRelay/HybridConnection) için birincil ve ikincil bağlantı dizelerini alır.</span><span class="sxs-lookup"><span data-stu-id="57430-103">Gets the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="57430-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="57430-104">SYNTAX</span></span>

### <span data-ttu-id="57430-105">NamespaceAuthorizationRuleSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="57430-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57430-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="57430-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57430-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="57430-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57430-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="57430-108">DESCRIPTION</span></span>
<span data-ttu-id="57430-109">**Get-AzRelayKey** cmdlet 'ı verilen geçiş varlıkları (Namespace/WcfRelay/HybridConnection) için birincil ve ikincil bağlantı dizelerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="57430-109">The **Get-AzRelayKey** cmdlet returns the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="57430-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="57430-110">EXAMPLES</span></span>

### <span data-ttu-id="57430-111">Örnek 1-ad alanı</span><span class="sxs-lookup"><span data-stu-id="57430-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="57430-112">Örnek 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="57430-112">Example 2 - WcfRelay</span></span>
```
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1  -WcfRelay TestWCFRelay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="57430-113">Örnek 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="57430-113">Example 3 - HybridConnection</span></span>
```
PS C:\> Get-AzRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="57430-114">Belirtilen geçiş varlıklarına (Namespace/WcfRelay/HybridConnection) birincil ve ikincil bağlantı dizesi.</span><span class="sxs-lookup"><span data-stu-id="57430-114">Primary and secondary connection string to the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="57430-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="57430-115">PARAMETERS</span></span>

### <span data-ttu-id="57430-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57430-116">-DefaultProfile</span></span>
<span data-ttu-id="57430-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="57430-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57430-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="57430-118">-HybridConnection</span></span>
<span data-ttu-id="57430-119">HybridConnection adı.</span><span class="sxs-lookup"><span data-stu-id="57430-119">HybridConnection Name.</span></span>

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

### <span data-ttu-id="57430-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="57430-120">-Name</span></span>
<span data-ttu-id="57430-121">AuthorizationRule adı.</span><span class="sxs-lookup"><span data-stu-id="57430-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="57430-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="57430-122">-Namespace</span></span>
<span data-ttu-id="57430-123">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="57430-123">Namespace Name.</span></span>

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

### <span data-ttu-id="57430-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57430-124">-ResourceGroupName</span></span>
<span data-ttu-id="57430-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="57430-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="57430-126">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="57430-126">-WcfRelay</span></span>
<span data-ttu-id="57430-127">WcfRelay adı.</span><span class="sxs-lookup"><span data-stu-id="57430-127">WcfRelay Name.</span></span>

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

### <span data-ttu-id="57430-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57430-128">CommonParameters</span></span>
<span data-ttu-id="57430-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="57430-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57430-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57430-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57430-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="57430-131">INPUTS</span></span>

### <span data-ttu-id="57430-132">System. String</span><span class="sxs-lookup"><span data-stu-id="57430-132">System.String</span></span>

## <span data-ttu-id="57430-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="57430-133">OUTPUTS</span></span>

### <span data-ttu-id="57430-134">Microsoft. Azure. Commands. Relay. modeller. PSAuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="57430-134">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span></span>

## <span data-ttu-id="57430-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="57430-135">NOTES</span></span>

## <span data-ttu-id="57430-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="57430-136">RELATED LINKS</span></span>
