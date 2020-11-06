---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespaceKey.md
ms.openlocfilehash: 5b366a3be8ca715a42c1c1f916d8ebf327dff8fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592548"
---
# <span data-ttu-id="d404c-101">New-AzureRmServiceBusNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="d404c-101">New-AzureRmServiceBusNamespaceKey</span></span>

## <span data-ttu-id="d404c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d404c-102">SYNOPSIS</span></span>
<span data-ttu-id="d404c-103">Hizmet veri yolu ad alanı için birincil veya ikincil bağlantı dizelerini yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d404c-103">Regenerates the primary or secondary connection strings for the Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d404c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d404c-104">SYNTAX</span></span>

```
New-AzureRmServiceBusNamespaceKey [-ResourceGroup] <String> -Namespace <String> -Name <String>
 [-RegenerateKeys] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d404c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d404c-105">DESCRIPTION</span></span>
<span data-ttu-id="d404c-106">**Yeni-AzureRmServiceBusNamespace** cmdlet 'i, belirtilen ad alanı ve yetkilendirme kuralı için yeni birincil veya ikincil bağlantı dizeleri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d404c-106">The **New-AzureRmServiceBusNamespace** cmdlet generates new primary or secondary connection strings for the specified namespace and authorization rule.</span></span>

## <span data-ttu-id="d404c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d404c-107">EXAMPLES</span></span>

### <span data-ttu-id="d404c-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d404c-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusNamespaceKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="d404c-109">Ad alanı için birincil veya ikincil bağlantı dizelerini yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d404c-109">Regenerates the primary or secondary connection strings for the namespace.</span></span>

## <span data-ttu-id="d404c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d404c-110">PARAMETERS</span></span>

### <span data-ttu-id="d404c-111">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="d404c-111">-RegenerateKeys</span></span>
<span data-ttu-id="d404c-112">Anahtarı yeniden üret: PrimaryKey/SecondaryKey.</span><span class="sxs-lookup"><span data-stu-id="d404c-112">Regenerate Keys: PrimaryKey/SecondaryKey.</span></span>

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

### <span data-ttu-id="d404c-113">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d404c-113">-ResourceGroup</span></span>
<span data-ttu-id="d404c-114">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d404c-114">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d404c-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="d404c-115">-Confirm</span></span>
<span data-ttu-id="d404c-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d404c-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d404c-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d404c-117">-WhatIf</span></span>
<span data-ttu-id="d404c-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d404c-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d404c-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d404c-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d404c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d404c-120">-DefaultProfile</span></span>
<span data-ttu-id="d404c-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d404c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d404c-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="d404c-122">-Name</span></span>
<span data-ttu-id="d404c-123">Yetkilendirme kuralı adı.</span><span class="sxs-lookup"><span data-stu-id="d404c-123">Authorization Rule Name.</span></span>

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

### <span data-ttu-id="d404c-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d404c-124">-Namespace</span></span>
<span data-ttu-id="d404c-125">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="d404c-125">Namespace Name.</span></span>

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

### <span data-ttu-id="d404c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d404c-126">CommonParameters</span></span>
<span data-ttu-id="d404c-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d404c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d404c-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d404c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d404c-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d404c-129">INPUTS</span></span>

### <span data-ttu-id="d404c-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d404c-130">-ResourceGroup</span></span>
 <span data-ttu-id="d404c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="d404c-131">System.String</span></span>
 

### <span data-ttu-id="d404c-132">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="d404c-132">-NamespaceName</span></span>
 <span data-ttu-id="d404c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d404c-133">System.String</span></span>
 

### <span data-ttu-id="d404c-134">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="d404c-134">-AuthorizationRuleName</span></span>
 <span data-ttu-id="d404c-135">System. String</span><span class="sxs-lookup"><span data-stu-id="d404c-135">System.String</span></span>
 

### <span data-ttu-id="d404c-136">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="d404c-136">-RegenerateKeys</span></span>
 <span data-ttu-id="d404c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d404c-137">System.String</span></span>

## <span data-ttu-id="d404c-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d404c-138">OUTPUTS</span></span>

### <span data-ttu-id="d404c-139">Microsoft. Azure. Management. ServiceBus. model. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="d404c-139">Microsoft.Azure.Management.ServiceBus.Models.ResourceListKeys</span></span>
<span data-ttu-id="d404c-140">PrimaryConnectionString: Endpoint = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = {SharedAccessKey-Value} SecondaryConnectionString: Endpoint = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = {SharedAccessKey-Value} PrimaryKey: {PrimaryKey değeri} SecondaryKey: {SecondaryKey Value} AnahtarAdı: AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="d404c-140">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey={SharedAccessKey-value} SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey={SharedAccessKey-value} PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : AuthoRule1</span></span>

## <span data-ttu-id="d404c-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d404c-141">NOTES</span></span>

## <span data-ttu-id="d404c-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d404c-142">RELATED LINKS</span></span>

