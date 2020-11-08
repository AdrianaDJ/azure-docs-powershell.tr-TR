---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 6940e12f813cbc4292f02ab98f0b35774da67025
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274537"
---
# <span data-ttu-id="2d11d-101">Get-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2d11d-101">Get-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="2d11d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d11d-102">SYNOPSIS</span></span>
<span data-ttu-id="2d11d-103">Yetkilendirme kuralının ayrıntılarını alır veya yetkilendirme kuralları listesini alır.</span><span class="sxs-lookup"><span data-stu-id="2d11d-103">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

## <span data-ttu-id="2d11d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2d11d-104">SYNTAX</span></span>

### <span data-ttu-id="2d11d-105">NamespaceAuthorizationRuleSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2d11d-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d11d-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="2d11d-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Eventhub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d11d-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="2d11d-107">AliasAuthoRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d11d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2d11d-108">DESCRIPTION</span></span>
<span data-ttu-id="2d11d-109">Get-AzEventHubAuthorizationRule cmdlet 'i, belirli bir olay hub 'ına yönelik tüm yetkilendirme kurallarının ayrıntılarını veya bir listesini alır.</span><span class="sxs-lookup"><span data-stu-id="2d11d-109">The Get-AzEventHubAuthorizationRule cmdlet gets either the details of an authorization rule, or a list of all authorization rules for a specified Event Hub.</span></span>
<span data-ttu-id="2d11d-110">Yetkilendirme kuralının adı sağlanmışsa, bu tek yetkilendirme kuralının ayrıntıları döndürülür.</span><span class="sxs-lookup"><span data-stu-id="2d11d-110">If the name of an authorization rule is provided, the details of that single authorization rule are returned.</span></span>
<span data-ttu-id="2d11d-111">Yetkilendirme kuralının adı sağlanmadıysa, belirtilen olay hub 'ına yönelik tüm yetkilendirme kurallarının bir listesi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="2d11d-111">If the name of an authorization rule is not provided, a list of all authorization rules for the specified Event Hub is returned.</span></span>
<span data-ttu-id="2d11d-112">Eğer (olağanüstü durum kurtarma) diğer adı sağlanmışsa, yapılandırılmış olan diğer ad alanının yetkilendirme kuralı ayrıntıları döndürülür.</span><span class="sxs-lookup"><span data-stu-id="2d11d-112">If (Disaster Recovery) Alias name provided, the details of authorization rule of the Namespace for Alias configured is returned.</span></span>

## <span data-ttu-id="2d11d-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2d11d-113">EXAMPLES</span></span>

### <span data-ttu-id="2d11d-114">Örnek 1: ad alanı için AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2d11d-114">Example 1: AuthorizationRule for namespace</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="2d11d-115">\` \` Minamespacename ad alanındaki cyauthrulename yetkilendirme kuralını alır \` \` .</span><span class="sxs-lookup"><span data-stu-id="2d11d-115">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="2d11d-116">Örnek 2: ad alanı için AuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="2d11d-116">Example 2: AuthorizationRules for namespace</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="2d11d-117">Mynamespacadındaki tüm yetkilendirme kurallarının bir listesini alır \` \` .</span><span class="sxs-lookup"><span data-stu-id="2d11d-117">Gets a list of all authorization rules in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="2d11d-118">Örnek 3: EventHub için AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2d11d-118">Example 3: AuthorizationRule for EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="2d11d-119">\` \` \` \` Minamespacename ad alanı tarafından kapsanan Olay Hub myeventhubname yetkilendirme kuralı \` \`</span><span class="sxs-lookup"><span data-stu-id="2d11d-119">Gets the authorization rule \`MyAuthRuleName\` in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="2d11d-120">Örnek 4: EventHub için AuthorizationRules</span><span class="sxs-lookup"><span data-stu-id="2d11d-120">Example 4: AuthorizationRules for EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="2d11d-121">Ad doğrulama kurallarını, \` \` ad alanı \` mynamespacename olan olay hub myeventhubname 'e alır \` .</span><span class="sxs-lookup"><span data-stu-id="2d11d-121">Gets list authorization rules in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="2d11d-122">Örnek 5: diğer ad için Authorizationkuralı (GeoRecovery yapılandırması)</span><span class="sxs-lookup"><span data-stu-id="2d11d-122">Example 5: AuthorizationRule for Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName -Name MyAuthRuleName
```

<span data-ttu-id="2d11d-123">\` \` Minamespacename ad alanındaki cyauthrulename yetkilendirme kuralını alır \` \` .</span><span class="sxs-lookup"><span data-stu-id="2d11d-123">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="2d11d-124">Örnek 6: diğer ad için Authorizationkuralları (GeoRecovery yapılandırması)</span><span class="sxs-lookup"><span data-stu-id="2d11d-124">Example 6: AuthorizationRules for Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName
```

<span data-ttu-id="2d11d-125">\` \` Mynamespacename ad alanındaki tüm yetkilendirme kuralı myauthrulename listesini alır \` \` .</span><span class="sxs-lookup"><span data-stu-id="2d11d-125">Gets a list of all authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="2d11d-126">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2d11d-126">PARAMETERS</span></span>

### <span data-ttu-id="2d11d-127">-Diğerad</span><span class="sxs-lookup"><span data-stu-id="2d11d-127">-AliasName</span></span>
<span data-ttu-id="2d11d-128">Diğer ad</span><span class="sxs-lookup"><span data-stu-id="2d11d-128">Alias Name</span></span>

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

### <span data-ttu-id="2d11d-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d11d-129">-DefaultProfile</span></span>
<span data-ttu-id="2d11d-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2d11d-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d11d-131">-Eventhub</span><span class="sxs-lookup"><span data-stu-id="2d11d-131">-Eventhub</span></span>
<span data-ttu-id="2d11d-132">Eventhub adı</span><span class="sxs-lookup"><span data-stu-id="2d11d-132">Eventhub Name</span></span>

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

### <span data-ttu-id="2d11d-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="2d11d-133">-Name</span></span>
<span data-ttu-id="2d11d-134">AuthorizationRule adı</span><span class="sxs-lookup"><span data-stu-id="2d11d-134">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d11d-135">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2d11d-135">-Namespace</span></span>
<span data-ttu-id="2d11d-136">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="2d11d-136">Namespace Name</span></span>

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

### <span data-ttu-id="2d11d-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d11d-137">-ResourceGroupName</span></span>
<span data-ttu-id="2d11d-138">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="2d11d-138">Resource Group Name</span></span>

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

### <span data-ttu-id="2d11d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d11d-139">CommonParameters</span></span>
<span data-ttu-id="2d11d-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2d11d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d11d-141">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d11d-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d11d-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2d11d-142">INPUTS</span></span>

### <span data-ttu-id="2d11d-143">System. String</span><span class="sxs-lookup"><span data-stu-id="2d11d-143">System.String</span></span>

## <span data-ttu-id="2d11d-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2d11d-144">OUTPUTS</span></span>

### <span data-ttu-id="2d11d-145">Microsoft. Azure. Commands. EventHub. model. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="2d11d-145">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="2d11d-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2d11d-146">NOTES</span></span>

## <span data-ttu-id="2d11d-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2d11d-147">RELATED LINKS</span></span>
