---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 86D8965D-D999-48A4-A4EE-9E054E5486EE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermaduser
schema: 2.0.0
ms.openlocfilehash: 5a1f0b5bac62c4b10912fbbffc07cda7c1f2fb7b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939669"
---
# <span data-ttu-id="db9e1-101">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="db9e1-101">New-AzureRmADUser</span></span>

## <span data-ttu-id="db9e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db9e1-102">SYNOPSIS</span></span>
<span data-ttu-id="db9e1-103">Yeni bir Active Directory kullanıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="db9e1-103">Creates a new active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db9e1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="db9e1-104">SYNTAX</span></span>

```
New-AzureRmADUser -DisplayName <String> -UserPrincipalName <String> -Password <SecureString>
 [-ImmutableId <String>] [-MailNickname <String>] [-ForceChangePasswordNextLogin]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db9e1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="db9e1-105">DESCRIPTION</span></span>
<span data-ttu-id="db9e1-106">Yeni bir Active Directory kullanıcısı (iş/okul hesabı, ayrıca org-ID olarak da bilinir) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="db9e1-106">Creates a new active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="db9e1-107">Daha fazla bilgi için: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span><span class="sxs-lookup"><span data-stu-id="db9e1-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span></span>

## <span data-ttu-id="db9e1-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="db9e1-108">EXAMPLES</span></span>

### <span data-ttu-id="db9e1-109">Örnek 1-yeni bir AD kullanıcısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="db9e1-109">Example 1 - Create a new AD user</span></span>
```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzureRmADUser -DisplayName "MyDisplayName" -UserPrincipalName "myemail@domain.com" -Password $SecureStringPassword -MailNickname "MyMailNickName"
```

<span data-ttu-id="db9e1-110">Kiracıda "MyDisplayName" ve Kullanıcı asıl adı "" adlı yeni bir AD kullanıcısı oluşturur myemail@domain.com .</span><span class="sxs-lookup"><span data-stu-id="db9e1-110">Creates a new AD user with the name "MyDisplayName" and user principal name "myemail@domain.com" in a tenant.</span></span>

## <span data-ttu-id="db9e1-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="db9e1-111">PARAMETERS</span></span>

### <span data-ttu-id="db9e1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db9e1-112">-DefaultProfile</span></span>
<span data-ttu-id="db9e1-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="db9e1-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db9e1-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="db9e1-114">-DisplayName</span></span>
<span data-ttu-id="db9e1-115">Kullanıcının adres defterinde görüntülenecek ad.</span><span class="sxs-lookup"><span data-stu-id="db9e1-115">The name to display in the address book for the user.</span></span>
<span data-ttu-id="db9e1-116">örnek ' Alex Wu '.</span><span class="sxs-lookup"><span data-stu-id="db9e1-116">example 'Alex Wu'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db9e1-117">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="db9e1-117">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="db9e1-118">Kullanıcının sonraki başarılı oturum açmada parolasını değiştirmesi gerekiyorsa belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="db9e1-118">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="db9e1-119">Sonraki başarılı oturum açmada parola değişimi için varsayılan davranış (false) olur.</span><span class="sxs-lookup"><span data-stu-id="db9e1-119">Default behavior is (false) to not change the password on the next successful login.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db9e1-120">-Sanmutableıd</span><span class="sxs-lookup"><span data-stu-id="db9e1-120">-ImmutableId</span></span>
<span data-ttu-id="db9e1-121">Yalnızca kullanıcının Kullanıcı asıl adı (UPN) özelliği için federe bir etki alanı kullanıyorsanız belirtilmesi gerekmektedir.</span><span class="sxs-lookup"><span data-stu-id="db9e1-121">It needs to be specified only if you are using a federated domain for the user's user principal name (upn) property.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db9e1-122">-Posta takma adı</span><span class="sxs-lookup"><span data-stu-id="db9e1-122">-MailNickname</span></span>
<span data-ttu-id="db9e1-123">Kullanıcının posta diğer adı.</span><span class="sxs-lookup"><span data-stu-id="db9e1-123">The mail alias for the user.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db9e1-124">-Parola</span><span class="sxs-lookup"><span data-stu-id="db9e1-124">-Password</span></span>
<span data-ttu-id="db9e1-125">Kullanıcının parolası.</span><span class="sxs-lookup"><span data-stu-id="db9e1-125">Password for the user.</span></span>
<span data-ttu-id="db9e1-126">Kiracının parola karmaşıklığı gereksinimlerini karşılamalıdır.</span><span class="sxs-lookup"><span data-stu-id="db9e1-126">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="db9e1-127">Güçlü bir parola ayarlamanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="db9e1-127">It is recommended to set a strong password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db9e1-128">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="db9e1-128">-UserPrincipalName</span></span>
<span data-ttu-id="db9e1-129">Kullanıcı asıl adı.</span><span class="sxs-lookup"><span data-stu-id="db9e1-129">The user principal name.</span></span>
<span data-ttu-id="db9e1-130">Örnek-' someuser@contoso.com '.</span><span class="sxs-lookup"><span data-stu-id="db9e1-130">Example-'someuser@contoso.com'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db9e1-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="db9e1-131">-Confirm</span></span>
<span data-ttu-id="db9e1-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="db9e1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db9e1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db9e1-133">-WhatIf</span></span>
<span data-ttu-id="db9e1-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="db9e1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db9e1-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="db9e1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db9e1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db9e1-136">CommonParameters</span></span>
<span data-ttu-id="db9e1-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="db9e1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db9e1-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db9e1-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db9e1-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="db9e1-139">INPUTS</span></span>

### <span data-ttu-id="db9e1-140">System. String</span><span class="sxs-lookup"><span data-stu-id="db9e1-140">System.String</span></span>

### <span data-ttu-id="db9e1-141">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="db9e1-141">System.Security.SecureString</span></span>

### <span data-ttu-id="db9e1-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="db9e1-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="db9e1-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="db9e1-143">OUTPUTS</span></span>

### <span data-ttu-id="db9e1-144">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="db9e1-144">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="db9e1-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="db9e1-145">NOTES</span></span>

## <span data-ttu-id="db9e1-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="db9e1-146">RELATED LINKS</span></span>

[<span data-ttu-id="db9e1-147">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="db9e1-147">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)



[<span data-ttu-id="db9e1-148">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="db9e1-148">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)
