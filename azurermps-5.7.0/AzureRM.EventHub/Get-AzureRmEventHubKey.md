---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
ms.openlocfilehash: f8a9f074398df5ce9d8464adf3c22a65d14784b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593491"
---
# <span data-ttu-id="d2dfc-101">Get-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="d2dfc-101">Get-AzureRmEventHubKey</span></span>

## <span data-ttu-id="d2dfc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2dfc-102">SYNOPSIS</span></span>
<span data-ttu-id="d2dfc-103">Belirtilen olay hub yetkilendirme kuralının birincil anahtar ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="d2dfc-103">Gets the primary key details of the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2dfc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d2dfc-104">SYNTAX</span></span>

### <span data-ttu-id="d2dfc-105">NamespaceAuthorizationRuleSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d2dfc-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2dfc-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="d2dfc-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2dfc-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="d2dfc-107">AliasAuthoRuleSet</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2dfc-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d2dfc-108">DESCRIPTION</span></span>
<span data-ttu-id="d2dfc-109">Get-AzureRmEventHubKey cmdlet 'i, belirtilen ad alanı/olay hub/diğer ad doğrulama kuralının birincil ve Ikincil ConnectionString ve anahtar ayrıntılarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="d2dfc-109">The Get-AzureRmEventHubKey cmdlet returns Primary and Secondary connectionstrings and keys details of the specified NameSpace/Event Hubs/Alias authorization rule.</span></span>

## <span data-ttu-id="d2dfc-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d2dfc-110">EXAMPLES</span></span>

### <span data-ttu-id="d2dfc-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d2dfc-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="d2dfc-112">Birincil ve Ikincil ConnectionString 'in ayrıntılarını ve \` myauthrulename yetkilendirme kuralı için anahtarları alır \` .</span><span class="sxs-lookup"><span data-stu-id="d2dfc-112">Gets details of Primary and Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="d2dfc-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d2dfc-113">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AliasName MyAliasName -Name MyAuthRuleName
```

<span data-ttu-id="d2dfc-114">Birincil, Ikincil, AliasPrimary ve diğerad Ikincil ConnectionString ve anahtar \` \`</span><span class="sxs-lookup"><span data-stu-id="d2dfc-114">Gets details of Primary, Secondary, AliasPrimary and AliasSecondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="d2dfc-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d2dfc-115">PARAMETERS</span></span>

### <span data-ttu-id="d2dfc-116">-Diğerad</span><span class="sxs-lookup"><span data-stu-id="d2dfc-116">-AliasName</span></span>
<span data-ttu-id="d2dfc-117">Diğer ad</span><span class="sxs-lookup"><span data-stu-id="d2dfc-117">Alias Name</span></span>

```yaml
Type: String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2dfc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2dfc-118">-DefaultProfile</span></span>
<span data-ttu-id="d2dfc-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d2dfc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2dfc-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="d2dfc-120">-EventHub</span></span>
<span data-ttu-id="d2dfc-121">EventHub adı</span><span class="sxs-lookup"><span data-stu-id="d2dfc-121">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2dfc-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="d2dfc-122">-Name</span></span>
<span data-ttu-id="d2dfc-123">AuthorizationRule adı</span><span class="sxs-lookup"><span data-stu-id="d2dfc-123">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2dfc-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d2dfc-124">-Namespace</span></span>
<span data-ttu-id="d2dfc-125">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="d2dfc-125">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2dfc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2dfc-126">-ResourceGroupName</span></span>
<span data-ttu-id="d2dfc-127">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="d2dfc-127">Resource Group Name</span></span>

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

### <span data-ttu-id="d2dfc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2dfc-128">CommonParameters</span></span>
<span data-ttu-id="d2dfc-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d2dfc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d2dfc-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2dfc-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2dfc-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d2dfc-131">INPUTS</span></span>

### <span data-ttu-id="d2dfc-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d2dfc-132">System.String</span></span>


## <span data-ttu-id="d2dfc-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d2dfc-133">OUTPUTS</span></span>

### <span data-ttu-id="d2dfc-134">Microsoft. Azure. Commands. EventHub. modeller. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="d2dfc-134">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>


## <span data-ttu-id="d2dfc-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d2dfc-135">NOTES</span></span>

## <span data-ttu-id="d2dfc-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d2dfc-136">RELATED LINKS</span></span>
