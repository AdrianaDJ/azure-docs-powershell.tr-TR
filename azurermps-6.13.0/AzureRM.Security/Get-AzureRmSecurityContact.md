---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityContact.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityContact.md
ms.openlocfilehash: 3d27e9a7962e20dff0d6360eb11db6a49c61a06d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763798"
---
# <span data-ttu-id="d3062-101">Get-AzureRmSecurityContact</span><span class="sxs-lookup"><span data-stu-id="d3062-101">Get-AzureRmSecurityContact</span></span>

## <span data-ttu-id="d3062-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3062-102">SYNOPSIS</span></span>
<span data-ttu-id="d3062-103">Bu abonelikte yapılandırılmış güvenlik kişilerini alır</span><span class="sxs-lookup"><span data-stu-id="d3062-103">Gets security contacts that were configured on this subscription</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3062-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d3062-104">SYNTAX</span></span>

### <span data-ttu-id="d3062-105">SubscriptionScope (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d3062-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityContact [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3062-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="d3062-106">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityContact -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3062-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="d3062-107">ResourceId</span></span>
```
Get-AzureRmSecurityContact -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3062-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d3062-108">DESCRIPTION</span></span>
<span data-ttu-id="d3062-109">Bu abonelikte yapılandırılmış güvenlik kişilerini alır.</span><span class="sxs-lookup"><span data-stu-id="d3062-109">Gets security contacts that were configured on this subscription.</span></span>
<span data-ttu-id="d3062-110">Güvenlik kişisi, abonelikte gerçekleşecek güvenlik uyarıları hakkında bildirim alabilir.</span><span class="sxs-lookup"><span data-stu-id="d3062-110">The security contact can get notifications on security alerts that happen on the subscription.</span></span>

## <span data-ttu-id="d3062-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d3062-111">EXAMPLES</span></span>

### <span data-ttu-id="d3062-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d3062-112">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityContact
Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/default1
Name               : default1
Email              : ascasc@microsoft.com
Phone              : 123123123
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="d3062-113">Tüm yapılandırılmış güvenlik kişilerini abonelikle alır</span><span class="sxs-lookup"><span data-stu-id="d3062-113">Gets all the configured security contacts on the subscription</span></span>

## <span data-ttu-id="d3062-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d3062-114">PARAMETERS</span></span>

### <span data-ttu-id="d3062-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3062-115">-DefaultProfile</span></span>
<span data-ttu-id="d3062-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d3062-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3062-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="d3062-117">-Name</span></span>
<span data-ttu-id="d3062-118">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="d3062-118">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3062-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d3062-119">-ResourceId</span></span>
<span data-ttu-id="d3062-120">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d3062-120">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3062-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3062-121">CommonParameters</span></span>
<span data-ttu-id="d3062-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d3062-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3062-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3062-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3062-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d3062-124">INPUTS</span></span>

### <span data-ttu-id="d3062-125">System. String</span><span class="sxs-lookup"><span data-stu-id="d3062-125">System.String</span></span>

## <span data-ttu-id="d3062-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d3062-126">OUTPUTS</span></span>

### <span data-ttu-id="d3062-127">Microsoft. Azure. Commands. Security. model. Securitcontacts. Pssecuritycontacts</span><span class="sxs-lookup"><span data-stu-id="d3062-127">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="d3062-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d3062-128">NOTES</span></span>

## <span data-ttu-id="d3062-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d3062-129">RELATED LINKS</span></span>
