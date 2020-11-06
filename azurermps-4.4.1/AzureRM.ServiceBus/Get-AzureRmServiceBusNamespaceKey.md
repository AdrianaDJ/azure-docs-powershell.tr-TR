---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespaceKey.md
ms.openlocfilehash: 87dc2d1e372bdab6415a78e8c79ed0c3bd5491ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590628"
---
# <span data-ttu-id="71ed5-101">Get-AzureRmServiceBusNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="71ed5-101">Get-AzureRmServiceBusNamespaceKey</span></span>

## <span data-ttu-id="71ed5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71ed5-102">SYNOPSIS</span></span>
<span data-ttu-id="71ed5-103">Ad alanı için birincil ve ikincil bağlantı dizelerini alır.</span><span class="sxs-lookup"><span data-stu-id="71ed5-103">Gets the primary and secondary connection strings for the namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71ed5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="71ed5-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusNamespaceKey [-ResourceGroup] <String> -Namespace <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71ed5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="71ed5-105">DESCRIPTION</span></span>
<span data-ttu-id="71ed5-106">**Get-AzureRmServiceBusNamespaceKey** cmdlet 'i, verilen ad alanı için birincil ve ikincil bağlantı dizelerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="71ed5-106">The **Get-AzureRmServiceBusNamespaceKey** cmdlet returns the primary and secondary connection strings for the given namespace.</span></span> 

## <span data-ttu-id="71ed5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="71ed5-107">EXAMPLES</span></span>

### <span data-ttu-id="71ed5-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="71ed5-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusNamespaceKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1
```

<span data-ttu-id="71ed5-109">Belirtilen ad alanına birincil ve ikincil bağlantı dizesi.</span><span class="sxs-lookup"><span data-stu-id="71ed5-109">Primary and secondary connection string to the specified namespace.</span></span>

## <span data-ttu-id="71ed5-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="71ed5-110">PARAMETERS</span></span>

### <span data-ttu-id="71ed5-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="71ed5-111">-ResourceGroup</span></span>
<span data-ttu-id="71ed5-112">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="71ed5-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="71ed5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71ed5-113">-DefaultProfile</span></span>
<span data-ttu-id="71ed5-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="71ed5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71ed5-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="71ed5-115">-Name</span></span>
<span data-ttu-id="71ed5-116">ServiceBus ad alanı Authorizationkural adı.</span><span class="sxs-lookup"><span data-stu-id="71ed5-116">ServiceBus Namespace AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="71ed5-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="71ed5-117">-Namespace</span></span>
<span data-ttu-id="71ed5-118">ServiceBus ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="71ed5-118">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="71ed5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71ed5-119">CommonParameters</span></span>
<span data-ttu-id="71ed5-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="71ed5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71ed5-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71ed5-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71ed5-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="71ed5-122">INPUTS</span></span>

### <span data-ttu-id="71ed5-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="71ed5-123">-ResourceGroup</span></span>
 <span data-ttu-id="71ed5-124">System. String</span><span class="sxs-lookup"><span data-stu-id="71ed5-124">System.String</span></span>
 

### <span data-ttu-id="71ed5-125">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="71ed5-125">-NamespaceName</span></span>
 <span data-ttu-id="71ed5-126">System. String</span><span class="sxs-lookup"><span data-stu-id="71ed5-126">System.String</span></span>
 

### <span data-ttu-id="71ed5-127">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="71ed5-127">-AuthorizationRuleName</span></span>
 <span data-ttu-id="71ed5-128">System. String</span><span class="sxs-lookup"><span data-stu-id="71ed5-128">System.String</span></span>

## <span data-ttu-id="71ed5-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="71ed5-129">OUTPUTS</span></span>

### <span data-ttu-id="71ed5-130">Microsoft. Azure. Management. ServiceBus. model. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="71ed5-130">Microsoft.Azure.Management.ServiceBus.Models.ResourceListKeys</span></span>
<span data-ttu-id="71ed5-131">PrimaryConnectionString: Endpoint = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = {SharedAccessKey Value} SecondaryConnectionString: Endpoint = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = AuthoRule1; SharedAccessKey = {SharedAccessKey Value} PrimaryKey: {PrimaryKey değeri} SecondaryKey: {SecondaryKey Value} AnahtarAdı: AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="71ed5-131">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey={SharedAccessKey value} SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey={SharedAccessKey value} PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : AuthoRule1</span></span>

## <span data-ttu-id="71ed5-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="71ed5-132">NOTES</span></span>

## <span data-ttu-id="71ed5-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="71ed5-133">RELATED LINKS</span></span>

