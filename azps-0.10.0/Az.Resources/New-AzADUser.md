---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 86D8965D-D999-48A4-A4EE-9E054E5486EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADUser.md
ms.openlocfilehash: f7127b97790736e69dd138b861b5239a907ab4e7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936403"
---
# <span data-ttu-id="6fed2-101">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="6fed2-101">New-AzADUser</span></span>

## <span data-ttu-id="6fed2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fed2-102">SYNOPSIS</span></span>
<span data-ttu-id="6fed2-103">Yeni bir Active Directory kullanıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6fed2-103">Creates a new active directory user.</span></span>

## <span data-ttu-id="6fed2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6fed2-104">SYNTAX</span></span>

```
New-AzADUser -DisplayName <String> -UserPrincipalName <String> -Password <SecureString>
 [-ImmutableId <String>] [-MailNickname <String>] [-ForceChangePasswordNextLogin]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fed2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6fed2-105">DESCRIPTION</span></span>
<span data-ttu-id="6fed2-106">Yeni bir Active Directory kullanıcısı (iş/okul hesabı, ayrıca org-ID olarak da bilinir) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6fed2-106">Creates a new active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="6fed2-107">Daha fazla bilgi için: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span><span class="sxs-lookup"><span data-stu-id="6fed2-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span></span>

## <span data-ttu-id="6fed2-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6fed2-108">EXAMPLES</span></span>

### <span data-ttu-id="6fed2-109">Örnek 1-yeni bir AD kullanıcısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="6fed2-109">Example 1 - Create a new AD user</span></span>
```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADUser -DisplayName "MyDisplayName" -UserPrincipalName "myemail@domain.com" -Password $SecureStringPassword -MailNickname "MyMailNickName"
```

<span data-ttu-id="6fed2-110">Kiracıda "MyDisplayName" ve Kullanıcı asıl adı "" adlı yeni bir AD kullanıcısı oluşturur myemail@domain.com .</span><span class="sxs-lookup"><span data-stu-id="6fed2-110">Creates a new AD user with the name "MyDisplayName" and user principal name "myemail@domain.com" in a tenant.</span></span>

## <span data-ttu-id="6fed2-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6fed2-111">PARAMETERS</span></span>

### <span data-ttu-id="6fed2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fed2-112">-DefaultProfile</span></span>
<span data-ttu-id="6fed2-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="6fed2-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fed2-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6fed2-114">-DisplayName</span></span>
<span data-ttu-id="6fed2-115">Kullanıcının adres defterinde görüntülenecek ad.</span><span class="sxs-lookup"><span data-stu-id="6fed2-115">The name to display in the address book for the user.</span></span>
<span data-ttu-id="6fed2-116">örnek ' Alex Wu '.</span><span class="sxs-lookup"><span data-stu-id="6fed2-116">example 'Alex Wu'.</span></span>

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

### <span data-ttu-id="6fed2-117">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="6fed2-117">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="6fed2-118">Kullanıcının sonraki başarılı oturum açmada parolasını değiştirmesi gerekiyorsa belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="6fed2-118">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="6fed2-119">Sonraki başarılı oturum açmada parola değişimi için varsayılan davranış (false) olur.</span><span class="sxs-lookup"><span data-stu-id="6fed2-119">Default behavior is (false) to not change the password on the next successful login.</span></span>

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

### <span data-ttu-id="6fed2-120">-Sanmutableıd</span><span class="sxs-lookup"><span data-stu-id="6fed2-120">-ImmutableId</span></span>
<span data-ttu-id="6fed2-121">Yalnızca kullanıcının Kullanıcı asıl adı (UPN) özelliği için federe bir etki alanı kullanıyorsanız belirtilmesi gerekmektedir.</span><span class="sxs-lookup"><span data-stu-id="6fed2-121">It needs to be specified only if you are using a federated domain for the user's user principal name (upn) property.</span></span>

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

### <span data-ttu-id="6fed2-122">-Posta takma adı</span><span class="sxs-lookup"><span data-stu-id="6fed2-122">-MailNickname</span></span>
<span data-ttu-id="6fed2-123">Kullanıcının posta diğer adı.</span><span class="sxs-lookup"><span data-stu-id="6fed2-123">The mail alias for the user.</span></span>

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

### <span data-ttu-id="6fed2-124">-Parola</span><span class="sxs-lookup"><span data-stu-id="6fed2-124">-Password</span></span>
<span data-ttu-id="6fed2-125">Kullanıcının parolası.</span><span class="sxs-lookup"><span data-stu-id="6fed2-125">Password for the user.</span></span>
<span data-ttu-id="6fed2-126">Kiracının parola karmaşıklığı gereksinimlerini karşılamalıdır.</span><span class="sxs-lookup"><span data-stu-id="6fed2-126">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="6fed2-127">Güçlü bir parola ayarlamanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="6fed2-127">It is recommended to set a strong password.</span></span>

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

### <span data-ttu-id="6fed2-128">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="6fed2-128">-UserPrincipalName</span></span>
<span data-ttu-id="6fed2-129">Kullanıcı asıl adı.</span><span class="sxs-lookup"><span data-stu-id="6fed2-129">The user principal name.</span></span>
<span data-ttu-id="6fed2-130">Örnek-' someuser@contoso.com '.</span><span class="sxs-lookup"><span data-stu-id="6fed2-130">Example-'someuser@contoso.com'.</span></span>

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

### <span data-ttu-id="6fed2-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="6fed2-131">-Confirm</span></span>
<span data-ttu-id="6fed2-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6fed2-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fed2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fed2-133">-WhatIf</span></span>
<span data-ttu-id="6fed2-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6fed2-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fed2-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6fed2-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fed2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fed2-136">CommonParameters</span></span>
<span data-ttu-id="6fed2-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6fed2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fed2-138">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fed2-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fed2-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6fed2-139">INPUTS</span></span>

### <span data-ttu-id="6fed2-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6fed2-140">System.String</span></span>

### <span data-ttu-id="6fed2-141">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="6fed2-141">System.Security.SecureString</span></span>

### <span data-ttu-id="6fed2-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6fed2-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6fed2-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6fed2-143">OUTPUTS</span></span>

### <span data-ttu-id="6fed2-144">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="6fed2-144">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="6fed2-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6fed2-145">NOTES</span></span>

## <span data-ttu-id="6fed2-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6fed2-146">RELATED LINKS</span></span>

[<span data-ttu-id="6fed2-147">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="6fed2-147">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="6fed2-148">Set-AzADUser</span><span class="sxs-lookup"><span data-stu-id="6fed2-148">Set-AzADUser</span></span>](./Set-AzADUser.md)

[<span data-ttu-id="6fed2-149">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="6fed2-149">Remove-AzADUser</span></span>](./Remove-AzADUser.md)