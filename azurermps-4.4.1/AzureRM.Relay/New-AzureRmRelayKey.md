---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayKey.md
ms.openlocfilehash: 7394ec382105b1d05bed589be95630f68ab79ae1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593024"
---
# <span data-ttu-id="2f545-101">New-AzureRmRelayKey</span><span class="sxs-lookup"><span data-stu-id="2f545-101">New-AzureRmRelayKey</span></span>

## <span data-ttu-id="2f545-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f545-102">SYNOPSIS</span></span>
<span data-ttu-id="2f545-103">Verilen geçiş varlıkları (Namespace/WcfRelay/HybridConnection) için birincil veya ikincil bağlantı dizelerini yeniden oluşturur</span><span class="sxs-lookup"><span data-stu-id="2f545-103">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f545-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2f545-104">SYNTAX</span></span>

### <span data-ttu-id="2f545-105">NamespaceAuthorizationRuleSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2f545-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f545-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2f545-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f545-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2f545-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzureRmRelayKey [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2f545-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2f545-108">DESCRIPTION</span></span>
<span data-ttu-id="2f545-109">**New-AzureRmRelayKey** cmdlet 'ı verilen geçiş varlıkları (Namespace/WcfRelay/HybridConnection) için birincil ve ikincil bağlantı dizelerini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2f545-109">The **New-AzureRmRelayKey** cmdlet generates the primary and secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="2f545-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2f545-110">EXAMPLES</span></span>

### <span data-ttu-id="2f545-111">Örnek 1-ad alanı</span><span class="sxs-lookup"><span data-stu-id="2f545-111">Example 1 - Namespace</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -RegenerateKeys SecondaryKey
```

### <span data-ttu-id="2f545-112">Örnek 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="2f545-112">Example 2 - WcfRelay</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -WcfRelay TestWCFRelay1 -RegenerateKeys SecondaryKey
```

### <span data-ttu-id="2f545-113">Örnek 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="2f545-113">Example 3 - HybridConnection</span></span>
```
PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys PrimaryKey

PS C:\> New-AzureRmRelayKey -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -HybridConnection TestHybridConnection -RegenerateKeys SecondaryKey
```

<span data-ttu-id="2f545-114">Verilen geçiş varlıkları (Namespace/WcfRelay/HybridConnection) için birincil veya ikincil bağlantı dizelerini yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2f545-114">Regenerates the primary or secondary connection strings for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="2f545-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2f545-115">PARAMETERS</span></span>

### <span data-ttu-id="2f545-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="2f545-116">-Confirm</span></span>
<span data-ttu-id="2f545-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2f545-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f545-118">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="2f545-118">-HybridConnection</span></span>
<span data-ttu-id="2f545-119">HybridConnection adı.</span><span class="sxs-lookup"><span data-stu-id="2f545-119">HybridConnection Name.</span></span>

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

### <span data-ttu-id="2f545-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="2f545-120">-Name</span></span>
<span data-ttu-id="2f545-121">AuthorizationRule adı.</span><span class="sxs-lookup"><span data-stu-id="2f545-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="2f545-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2f545-122">-Namespace</span></span>
<span data-ttu-id="2f545-123">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="2f545-123">Namespace Name.</span></span>

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

### <span data-ttu-id="2f545-124">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="2f545-124">-RegenerateKey</span></span>
<span data-ttu-id="2f545-125">Anahtarları yeniden üret-' PrimaryKey '/' SecondaryKey '.</span><span class="sxs-lookup"><span data-stu-id="2f545-125">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

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

### <span data-ttu-id="2f545-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f545-126">-ResourceGroupName</span></span>
<span data-ttu-id="2f545-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="2f545-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="2f545-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="2f545-128">-WcfRelay</span></span>
<span data-ttu-id="2f545-129">WcfRelay adı.</span><span class="sxs-lookup"><span data-stu-id="2f545-129">WcfRelay Name.</span></span>

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

### <span data-ttu-id="2f545-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f545-130">-WhatIf</span></span>
<span data-ttu-id="2f545-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2f545-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f545-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2f545-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f545-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f545-133">-DefaultProfile</span></span>
<span data-ttu-id="2f545-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2f545-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f545-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f545-135">CommonParameters</span></span>
<span data-ttu-id="2f545-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2f545-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f545-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f545-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f545-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2f545-138">INPUTS</span></span>

### <span data-ttu-id="2f545-139">-Resourcegroupsüs adı</span><span class="sxs-lookup"><span data-stu-id="2f545-139">-ResourceGroupNameName</span></span>
 <span data-ttu-id="2f545-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2f545-140">System.String</span></span> 

### <span data-ttu-id="2f545-141">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="2f545-141">-NamespaceName</span></span>
 <span data-ttu-id="2f545-142">System. String</span><span class="sxs-lookup"><span data-stu-id="2f545-142">System.String</span></span> 
 

### <span data-ttu-id="2f545-143">-HybridConnectionsName</span><span class="sxs-lookup"><span data-stu-id="2f545-143">-HybridConnectionsName</span></span>
 <span data-ttu-id="2f545-144">System. String</span><span class="sxs-lookup"><span data-stu-id="2f545-144">System.String</span></span> 

### <span data-ttu-id="2f545-145">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="2f545-145">-WcfRelayName</span></span>
 <span data-ttu-id="2f545-146">System. String</span><span class="sxs-lookup"><span data-stu-id="2f545-146">System.String</span></span> 

### <span data-ttu-id="2f545-147">-Ad</span><span class="sxs-lookup"><span data-stu-id="2f545-147">-Name</span></span>
 <span data-ttu-id="2f545-148">System. String</span><span class="sxs-lookup"><span data-stu-id="2f545-148">System.String</span></span>

### <span data-ttu-id="2f545-149">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="2f545-149">-RegenerateKeys</span></span>
 <span data-ttu-id="2f545-150">System. String</span><span class="sxs-lookup"><span data-stu-id="2f545-150">System.String</span></span>

## <span data-ttu-id="2f545-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2f545-151">OUTPUTS</span></span>

### <span data-ttu-id="2f545-152">Microsoft. Azure. Commands. Relay. modeller. AuthorizationRuleKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="2f545-152">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleKeysAttributes</span></span>

### <span data-ttu-id="2f545-153">Örnek 1-ad alanı</span><span class="sxs-lookup"><span data-stu-id="2f545-153">Example 1 - Namespace</span></span>
<span data-ttu-id="2f545-154">PrimaryConnectionString: Endpoint = SB://TestNamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #</span><span class="sxs-lookup"><span data-stu-id="2f545-154">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################ PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="2f545-155">Örnek 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="2f545-155">Example 2 - WcfRelay</span></span>
<span data-ttu-id="2f545-156">PrimaryConnectionString: Endpoint = SB://TestNamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #; EntityPath = TestWCFRelay1 SecondaryConnectionString: Endpoint = SB://TestNamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #; EntityPath = TestWCFRelay1 PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #</span><span class="sxs-lookup"><span data-stu-id="2f545-156">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestWCFRelay1 PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

### <span data-ttu-id="2f545-157">Örnek 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="2f545-157">Example 3 - HybridConnection</span></span>
<span data-ttu-id="2f545-158">PrimaryConnectionString: Endpoint = SB://TestNamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #; EntityPath = TestHybridConnection SecondaryConnectionString: Endpoint = SB://TestNamespace-relay1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #; EntityPath = TestHybridConnection PrimaryKey: # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # # #</span><span class="sxs-lookup"><span data-stu-id="2f545-158">PrimaryConnectionString   : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection SecondaryConnectionString : Endpoint=sb://testnamespace-relay1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey=############################################;EntityPath=TestHybridConnection PrimaryKey                : ############################################ SecondaryKey              : ############################################ KeyName                   : AuthoRule1</span></span>

## <span data-ttu-id="2f545-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2f545-159">NOTES</span></span>

## <span data-ttu-id="2f545-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2f545-160">RELATED LINKS</span></span>

