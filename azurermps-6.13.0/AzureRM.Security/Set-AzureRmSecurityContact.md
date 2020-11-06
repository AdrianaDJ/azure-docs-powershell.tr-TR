---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityContact.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityContact.md
ms.openlocfilehash: 30586dcbbc08c31bf9b9fe65886fd2f487398618
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590029"
---
# <span data-ttu-id="a8198-101">Set-AzureRmSecurityContact</span><span class="sxs-lookup"><span data-stu-id="a8198-101">Set-AzureRmSecurityContact</span></span>

## <span data-ttu-id="a8198-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8198-102">SYNOPSIS</span></span>
<span data-ttu-id="a8198-103">Abonelik için bir güvenlik kişisi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a8198-103">Updates a security contact for a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8198-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a8198-104">SYNTAX</span></span>

```
Set-AzureRmSecurityContact -Name <String> -Email <String> -Phone <String> [-AlertAdmin] [-NotifyOnAlert]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8198-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a8198-105">DESCRIPTION</span></span>
<span data-ttu-id="a8198-106">Abonelik için bir güvenlik kişisi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a8198-106">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="a8198-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a8198-107">EXAMPLES</span></span>

### <span data-ttu-id="a8198-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a8198-108">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSecurityContact -Name "default1" -Email "john@contoso.com" -Phone "214275-4038" -AlertAdmin -NotifyOnAlert

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/
                     default1
Name               : default1
Email              : john@contoso.com
Phone              : 214275-4038
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="a8198-109">Abonelik için bir güvenlik kişisi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a8198-109">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="a8198-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a8198-110">PARAMETERS</span></span>

### <span data-ttu-id="a8198-111">-AlertAdmin</span><span class="sxs-lookup"><span data-stu-id="a8198-111">-AlertAdmin</span></span>
<span data-ttu-id="a8198-112">Yöneticilere uyarılar.</span><span class="sxs-lookup"><span data-stu-id="a8198-112">Alerts To Administrators.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8198-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8198-113">-DefaultProfile</span></span>
<span data-ttu-id="a8198-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a8198-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8198-115">-E-posta</span><span class="sxs-lookup"><span data-stu-id="a8198-115">-Email</span></span>
<span data-ttu-id="a8198-116">E-posta.</span><span class="sxs-lookup"><span data-stu-id="a8198-116">E-Mail.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8198-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="a8198-117">-Name</span></span>
<span data-ttu-id="a8198-118">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="a8198-118">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8198-119">-NotifyOnAlert</span><span class="sxs-lookup"><span data-stu-id="a8198-119">-NotifyOnAlert</span></span>
<span data-ttu-id="a8198-120">Uyarı bildirimleri.</span><span class="sxs-lookup"><span data-stu-id="a8198-120">Alert Notifications.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8198-121">-Telefon</span><span class="sxs-lookup"><span data-stu-id="a8198-121">-Phone</span></span>
<span data-ttu-id="a8198-122">Telefon.</span><span class="sxs-lookup"><span data-stu-id="a8198-122">Phone.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8198-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="a8198-123">-Confirm</span></span>
<span data-ttu-id="a8198-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a8198-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8198-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8198-125">-WhatIf</span></span>
<span data-ttu-id="a8198-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a8198-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a8198-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a8198-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8198-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8198-128">CommonParameters</span></span>
<span data-ttu-id="a8198-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a8198-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8198-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8198-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8198-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a8198-131">INPUTS</span></span>

### <span data-ttu-id="a8198-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a8198-132">System.String</span></span>

## <span data-ttu-id="a8198-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a8198-133">OUTPUTS</span></span>

### <span data-ttu-id="a8198-134">Microsoft. Azure. Commands. Security. model. Securitcontacts. Pssecuritycontacts</span><span class="sxs-lookup"><span data-stu-id="a8198-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="a8198-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a8198-135">NOTES</span></span>

## <span data-ttu-id="a8198-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a8198-136">RELATED LINKS</span></span>
