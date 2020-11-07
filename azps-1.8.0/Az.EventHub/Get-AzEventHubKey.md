---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubKey.md
ms.openlocfilehash: 143604052fbbec594af0093ee94cbbadafac14d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760847"
---
# <span data-ttu-id="6934a-101">Get-AzEventHubKey</span><span class="sxs-lookup"><span data-stu-id="6934a-101">Get-AzEventHubKey</span></span>

## <span data-ttu-id="6934a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6934a-102">SYNOPSIS</span></span>
<span data-ttu-id="6934a-103">Belirtilen olay hub yetkilendirme kuralının birincil anahtar ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="6934a-103">Gets the primary key details of the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="6934a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6934a-104">SYNTAX</span></span>

### <span data-ttu-id="6934a-105">NamespaceAuthorizationRuleSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6934a-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6934a-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="6934a-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6934a-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="6934a-107">AliasAuthoRuleSet</span></span>
```
Get-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6934a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6934a-108">DESCRIPTION</span></span>
<span data-ttu-id="6934a-109">Get-AzEventHubKey cmdlet 'i, belirtilen ad alanı/olay hub/diğer ad doğrulama kuralının birincil ve Ikincil ConnectionString ve anahtar ayrıntılarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="6934a-109">The Get-AzEventHubKey cmdlet returns Primary and Secondary connectionstrings and keys details of the specified NameSpace/Event Hubs/Alias authorization rule.</span></span>

## <span data-ttu-id="6934a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6934a-110">EXAMPLES</span></span>

### <span data-ttu-id="6934a-111">Örnek 1-ad alanı</span><span class="sxs-lookup"><span data-stu-id="6934a-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

### <span data-ttu-id="6934a-112">Örnek 2-EventHub</span><span class="sxs-lookup"><span data-stu-id="6934a-112">Example 2 - EventHub</span></span>
```
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="6934a-113">Birincil ve Ikincil ConnectionString 'in ayrıntılarını ve \` myauthrulename yetkilendirme kuralı için anahtarları alır \` .</span><span class="sxs-lookup"><span data-stu-id="6934a-113">Gets details of Primary and Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="6934a-114">Örnek 3-diğer ad (GeoRecovery yapılandırması)</span><span class="sxs-lookup"><span data-stu-id="6934a-114">Example 3 - Alias (GeoRecovery Configuration)</span></span>
```
PS C:\> Get-AzEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AliasName MyAliasName -Name MyAuthRuleName
```

<span data-ttu-id="6934a-115">Birincil, Ikincil, AliasPrimary ve diğerad Ikincil ConnectionString ve anahtar \` \`</span><span class="sxs-lookup"><span data-stu-id="6934a-115">Gets details of Primary, Secondary, AliasPrimary and AliasSecondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="6934a-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6934a-116">PARAMETERS</span></span>

### <span data-ttu-id="6934a-117">-Diğerad</span><span class="sxs-lookup"><span data-stu-id="6934a-117">-AliasName</span></span>
<span data-ttu-id="6934a-118">Diğer ad</span><span class="sxs-lookup"><span data-stu-id="6934a-118">Alias Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6934a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6934a-119">-DefaultProfile</span></span>
<span data-ttu-id="6934a-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6934a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6934a-121">-EventHub</span><span class="sxs-lookup"><span data-stu-id="6934a-121">-EventHub</span></span>
<span data-ttu-id="6934a-122">EventHub adı</span><span class="sxs-lookup"><span data-stu-id="6934a-122">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6934a-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="6934a-123">-Name</span></span>
<span data-ttu-id="6934a-124">AuthorizationRule adı</span><span class="sxs-lookup"><span data-stu-id="6934a-124">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6934a-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6934a-125">-Namespace</span></span>
<span data-ttu-id="6934a-126">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="6934a-126">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6934a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6934a-127">-ResourceGroupName</span></span>
<span data-ttu-id="6934a-128">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="6934a-128">Resource Group Name</span></span>

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

### <span data-ttu-id="6934a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6934a-129">CommonParameters</span></span>
<span data-ttu-id="6934a-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6934a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6934a-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6934a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6934a-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6934a-132">INPUTS</span></span>

### <span data-ttu-id="6934a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="6934a-133">System.String</span></span>

## <span data-ttu-id="6934a-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6934a-134">OUTPUTS</span></span>

### <span data-ttu-id="6934a-135">Microsoft. Azure. Commands. EventHub. modeller. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="6934a-135">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="6934a-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6934a-136">NOTES</span></span>

## <span data-ttu-id="6934a-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6934a-137">RELATED LINKS</span></span>