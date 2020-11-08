---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityContact.md
ms.openlocfilehash: e115e5dc9537ace9275517c74057e5f99d80e006
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097076"
---
# <span data-ttu-id="06597-101">Get-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="06597-101">Get-AzSecurityContact</span></span>

## <span data-ttu-id="06597-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06597-102">SYNOPSIS</span></span>
<span data-ttu-id="06597-103">Bu abonelikte yapılandırılmış güvenlik kişilerini alır</span><span class="sxs-lookup"><span data-stu-id="06597-103">Gets security contacts that were configured on this subscription</span></span>

## <span data-ttu-id="06597-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="06597-104">SYNTAX</span></span>

### <span data-ttu-id="06597-105">SubscriptionScope (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="06597-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityContact [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06597-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="06597-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityContact -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06597-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="06597-107">ResourceId</span></span>
```
Get-AzSecurityContact -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06597-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="06597-108">DESCRIPTION</span></span>
<span data-ttu-id="06597-109">Bu abonelikte yapılandırılmış güvenlik kişilerini alır.</span><span class="sxs-lookup"><span data-stu-id="06597-109">Gets security contacts that were configured on this subscription.</span></span>
<span data-ttu-id="06597-110">Güvenlik kişisi, abonelikte gerçekleşecek güvenlik uyarıları hakkında bildirim alabilir.</span><span class="sxs-lookup"><span data-stu-id="06597-110">The security contact can get notifications on security alerts that happen on the subscription.</span></span>

## <span data-ttu-id="06597-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="06597-111">EXAMPLES</span></span>

### <span data-ttu-id="06597-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="06597-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityContact
Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/default1
Name               : default1
Email              : ascasc@microsoft.com
Phone              : 123123123
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="06597-113">Tüm yapılandırılmış güvenlik kişilerini abonelikle alır</span><span class="sxs-lookup"><span data-stu-id="06597-113">Gets all the configured security contacts on the subscription</span></span>

## <span data-ttu-id="06597-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="06597-114">PARAMETERS</span></span>

### <span data-ttu-id="06597-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06597-115">-DefaultProfile</span></span>
<span data-ttu-id="06597-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="06597-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06597-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="06597-117">-Name</span></span>
<span data-ttu-id="06597-118">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="06597-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06597-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="06597-119">-ResourceId</span></span>
<span data-ttu-id="06597-120">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="06597-120">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06597-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06597-121">CommonParameters</span></span>
<span data-ttu-id="06597-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="06597-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06597-123">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06597-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06597-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="06597-124">INPUTS</span></span>

### <span data-ttu-id="06597-125">System. String</span><span class="sxs-lookup"><span data-stu-id="06597-125">System.String</span></span>

## <span data-ttu-id="06597-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="06597-126">OUTPUTS</span></span>

### <span data-ttu-id="06597-127">Microsoft. Azure. Commands. Security. model. Securitcontacts. Pssecuritycontacts</span><span class="sxs-lookup"><span data-stu-id="06597-127">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="06597-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="06597-128">NOTES</span></span>

## <span data-ttu-id="06597-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="06597-129">RELATED LINKS</span></span>