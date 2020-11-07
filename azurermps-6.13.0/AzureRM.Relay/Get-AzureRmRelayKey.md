---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermrelaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayKey.md
ms.openlocfilehash: 69f6b1bc50681bafe7a860dcebaa7616c8f14e90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764915"
---
# <span data-ttu-id="2eed5-101">Get-AzureRmRelayKey</span><span class="sxs-lookup"><span data-stu-id="2eed5-101">Get-AzureRmRelayKey</span></span>

## <span data-ttu-id="2eed5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2eed5-102">SYNOPSIS</span></span>
<span data-ttu-id="2eed5-103">Verilen geçiş varlıkları (Namespace/WcfRelay/HybridConnection) için birincil ve ikincil bağlantı dizelerini alır.</span><span class="sxs-lookup"><span data-stu-id="2eed5-103">Gets the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2eed5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2eed5-104">SYNTAX</span></span>

### <span data-ttu-id="2eed5-105">NamespaceAuthorizationRuleSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2eed5-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2eed5-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2eed5-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2eed5-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2eed5-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2eed5-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2eed5-108">DESCRIPTION</span></span>
<span data-ttu-id="2eed5-109">**Get-AzureRmRelayKey** cmdlet 'ı verilen geçiş varlıkları (Namespace/WcfRelay/HybridConnection) için birincil ve ikincil bağlantı dizelerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="2eed5-109">The **Get-AzureRmRelayKey** cmdlet returns the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="2eed5-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2eed5-110">EXAMPLES</span></span>

### <span data-ttu-id="2eed5-111">Örnek 1-ad alanı</span><span class="sxs-lookup"><span data-stu-id="2eed5-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="2eed5-112">Örnek 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="2eed5-112">Example 2 - WcfRelay</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1  -WcfRelay TestWCFRelay1 -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

### <span data-ttu-id="2eed5-113">Örnek 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="2eed5-113">Example 3 - HybridConnection</span></span>
```
PS C:\> Get-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1

PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection
PrimaryKey                : ############################################
SecondaryKey              : ############################################
KeyName                   : AuthoRule1
```

<span data-ttu-id="2eed5-114">Belirtilen geçiş varlıklarına (Namespace/WcfRelay/HybridConnection) birincil ve ikincil bağlantı dizesi.</span><span class="sxs-lookup"><span data-stu-id="2eed5-114">Primary and secondary connection string to the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="2eed5-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2eed5-115">PARAMETERS</span></span>

### <span data-ttu-id="2eed5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eed5-116">-DefaultProfile</span></span>
<span data-ttu-id="2eed5-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2eed5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2eed5-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="2eed5-118">-HybridConnection</span></span>
<span data-ttu-id="2eed5-119">HybridConnection adı.</span><span class="sxs-lookup"><span data-stu-id="2eed5-119">HybridConnection Name.</span></span>

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

### <span data-ttu-id="2eed5-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="2eed5-120">-Name</span></span>
<span data-ttu-id="2eed5-121">AuthorizationRule adı.</span><span class="sxs-lookup"><span data-stu-id="2eed5-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="2eed5-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2eed5-122">-Namespace</span></span>
<span data-ttu-id="2eed5-123">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="2eed5-123">Namespace Name.</span></span>

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

### <span data-ttu-id="2eed5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2eed5-124">-ResourceGroupName</span></span>
<span data-ttu-id="2eed5-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="2eed5-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="2eed5-126">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="2eed5-126">-WcfRelay</span></span>
<span data-ttu-id="2eed5-127">WcfRelay adı.</span><span class="sxs-lookup"><span data-stu-id="2eed5-127">WcfRelay Name.</span></span>

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

### <span data-ttu-id="2eed5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eed5-128">CommonParameters</span></span>
<span data-ttu-id="2eed5-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2eed5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2eed5-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2eed5-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eed5-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2eed5-131">INPUTS</span></span>

### <span data-ttu-id="2eed5-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2eed5-132">System.String</span></span>


## <span data-ttu-id="2eed5-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2eed5-133">OUTPUTS</span></span>

### <span data-ttu-id="2eed5-134">Microsoft. Azure. Commands. Relay. modeller. PSAuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="2eed5-134">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleKeysAttributes</span></span>


## <span data-ttu-id="2eed5-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2eed5-135">NOTES</span></span>

## <span data-ttu-id="2eed5-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2eed5-136">RELATED LINKS</span></span>
