---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopicKey.md
ms.openlocfilehash: ed31934a75d9d6826a7e0464dccd43fd2d853daa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589109"
---
# <span data-ttu-id="4768b-101">New-AzureRmServiceBusTopicKey</span><span class="sxs-lookup"><span data-stu-id="4768b-101">New-AzureRmServiceBusTopicKey</span></span>

## <span data-ttu-id="4768b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4768b-102">SYNOPSIS</span></span>
<span data-ttu-id="4768b-103">Service Bus konusunun birincil veya ikincil bağlantı dizelerini yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4768b-103">Regenerates the primary or secondary connection strings for the Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4768b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4768b-104">SYNTAX</span></span>

```
New-AzureRmServiceBusTopicKey [-ResourceGroup] <String> -Namespace <String> -Topic <String> -Name <String>
 [-RegenerateKeys] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4768b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4768b-105">DESCRIPTION</span></span>
<span data-ttu-id="4768b-106">**Yeni-AzureRmServiceBusTopicKey** cmdlet 'ı belirtilen hizmet veri yolu konusu ve yetkilendirme kuralı için yeni bir birincil veya ikincil bağlantı dizesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4768b-106">The **New-AzureRmServiceBusTopicKey** cmdlet generates a new primary or secondary connection string for the specified Service Bus topic and authorization rule.</span></span>

## <span data-ttu-id="4768b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4768b-107">EXAMPLES</span></span>

### <span data-ttu-id="4768b-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4768b-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusTopicKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="4768b-109">Ad alanı için birincil bağlantı dizesini yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4768b-109">Regenerates the primary connection string for the namespace.</span></span>

### <span data-ttu-id="4768b-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="4768b-110">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusTopicKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1 -RegenerateKeys SecondaryKey
```

<span data-ttu-id="4768b-111">Ad alanı için ikincil bağlantı dizesini yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4768b-111">Regenerates the secondary connection string for the namespace.</span></span>

## <span data-ttu-id="4768b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4768b-112">PARAMETERS</span></span>

### <span data-ttu-id="4768b-113">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="4768b-113">-RegenerateKeys</span></span>
<span data-ttu-id="4768b-114">Birincil veya ikincil anahtarların yeniden oluşturulup oluşturulmayacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4768b-114">Specifies whether to regenerate the primary or secondary keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4768b-115">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4768b-115">-ResourceGroup</span></span>
<span data-ttu-id="4768b-116">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4768b-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="4768b-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="4768b-117">-Confirm</span></span>
<span data-ttu-id="4768b-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4768b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4768b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4768b-119">-WhatIf</span></span>
<span data-ttu-id="4768b-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4768b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4768b-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4768b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4768b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4768b-122">-DefaultProfile</span></span>
<span data-ttu-id="4768b-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4768b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4768b-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="4768b-124">-Name</span></span>
<span data-ttu-id="4768b-125">Yetkilendirme kuralı adı.</span><span class="sxs-lookup"><span data-stu-id="4768b-125">Authorization Rule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4768b-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4768b-126">-Namespace</span></span>
<span data-ttu-id="4768b-127">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="4768b-127">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4768b-128">-Konu</span><span class="sxs-lookup"><span data-stu-id="4768b-128">-Topic</span></span>
<span data-ttu-id="4768b-129">Konu adı.</span><span class="sxs-lookup"><span data-stu-id="4768b-129">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4768b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4768b-130">CommonParameters</span></span>
<span data-ttu-id="4768b-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4768b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4768b-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4768b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4768b-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4768b-133">INPUTS</span></span>

### <span data-ttu-id="4768b-134">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4768b-134">-ResourceGroup</span></span>
 <span data-ttu-id="4768b-135">System. String</span><span class="sxs-lookup"><span data-stu-id="4768b-135">System.String</span></span>
 

### <span data-ttu-id="4768b-136">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="4768b-136">-NamespaceName</span></span>
 <span data-ttu-id="4768b-137">System. String</span><span class="sxs-lookup"><span data-stu-id="4768b-137">System.String</span></span>
 

### <span data-ttu-id="4768b-138">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="4768b-138">-AuthorizationRuleName</span></span>
 <span data-ttu-id="4768b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="4768b-139">System.String</span></span>
 

### <span data-ttu-id="4768b-140">-TopicName</span><span class="sxs-lookup"><span data-stu-id="4768b-140">-TopicName</span></span>
 <span data-ttu-id="4768b-141">System. String</span><span class="sxs-lookup"><span data-stu-id="4768b-141">System.String</span></span>
 

### <span data-ttu-id="4768b-142">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="4768b-142">-RegenerateKeys</span></span>
 <span data-ttu-id="4768b-143">System. String</span><span class="sxs-lookup"><span data-stu-id="4768b-143">System.String</span></span>

## <span data-ttu-id="4768b-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4768b-144">OUTPUTS</span></span>

### <span data-ttu-id="4768b-145">Microsoft. Azure. Commands. ServiceBus. modeller. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="4768b-145">Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes</span></span>
<span data-ttu-id="4768b-146">PrimaryConnectionString: Endpoint = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = SBTopicAuthoRule1; SharedAccessKey = {SharedAccessKey-Value}; EntityPath = SB-Topı c_exampl1 SecondaryConnectionString: Endpoint = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = SBTopicAuthoRule1; SharedAccessKey = {SharedAccessKey-Value}; EntityPath = SB-Topı c_exampl1 PrimaryKey: {PrimaryKey değeri} SecondaryKey: {SecondaryKey Value} AnahtarAdı: SBTopicAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="4768b-146">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBTopicAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Topi c_exampl1 SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBTopicAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Topi c_exampl1 PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : SBTopicAuthoRule1</span></span>

## <span data-ttu-id="4768b-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4768b-147">NOTES</span></span>

## <span data-ttu-id="4768b-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4768b-148">RELATED LINKS</span></span>

