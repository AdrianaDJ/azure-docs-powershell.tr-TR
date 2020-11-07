---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-Azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Update-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Update-AzADUser.md
ms.openlocfilehash: 2fe2162221672522596065ef615a8098bfc12a60
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936294"
---
# <span data-ttu-id="e45a9-101">Update-AzADUser</span><span class="sxs-lookup"><span data-stu-id="e45a9-101">Update-AzADUser</span></span>

## <span data-ttu-id="e45a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e45a9-102">SYNOPSIS</span></span>
<span data-ttu-id="e45a9-103">Var olan Active Directory kullanıcısını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e45a9-103">Updates an existing active directory user.</span></span>

## <span data-ttu-id="e45a9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e45a9-104">SYNTAX</span></span>

### <span data-ttu-id="e45a9-105">Upnorobjectivseçparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e45a9-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Update-AzADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e45a9-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="e45a9-106">UPNParameterSet</span></span>
```
Update-AzADUser -UserPrincipalName <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e45a9-107">NesneKimliği</span><span class="sxs-lookup"><span data-stu-id="e45a9-107">ObjectIdParameterSet</span></span>
```
Update-AzADUser -ObjectId <Guid> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e45a9-108">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="e45a9-108">InputObjectParameterSet</span></span>
```
Update-AzADUser -InputObject <PSADUser> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e45a9-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="e45a9-109">DESCRIPTION</span></span>
<span data-ttu-id="e45a9-110">Var olan Active Directory kullanıcısını (iş/okul hesabı da, org-ID olarak da bilinir) güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e45a9-110">Updates an existing active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="e45a9-111">Daha fazla bilgi için: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span><span class="sxs-lookup"><span data-stu-id="e45a9-111">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span></span>

## <span data-ttu-id="e45a9-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e45a9-112">EXAMPLES</span></span>

### <span data-ttu-id="e45a9-113">Örnek 1-nesne kimliği kullanan bir kullanıcının görünen adını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="e45a9-113">Example 1 - Update the display name of a user using object id</span></span>

```
PS C:\> Update-AzADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 -DisplayName MyNewDisplayName
```

<span data-ttu-id="e45a9-114">' 155a5c10-93a9-4941-a0df-96vseç83ab5ab24 ' nesnesi</span><span class="sxs-lookup"><span data-stu-id="e45a9-114">Updates the display name of the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="e45a9-115">Örnek 2-kullanıcının görünen adını Kullanıcı asıl adı kullanarak güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="e45a9-115">Example 2 - Update the display name of a user using user principal name</span></span>

```
PS C:\> Update-AzADUser -UserPrincipalName foo@domain.com -DisplayName MyNewDisplayName
```

<span data-ttu-id="e45a9-116">Kullanıcı asıl adı ' ' olan kullanıcının görünen adını foo@domain.com ' Yenisdisplayname ' olarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e45a9-116">Updates the display name of the user with user principal name 'foo@domain.com' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="e45a9-117">Örnek 3-boru kullanarak bir kullanıcının görünen adını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="e45a9-117">Example 3 - Update the display name of a user using piping</span></span>

```
PS C:\> Get-AzADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 | Update-AzADUser -DisplayName MyNewDisplayName
```

<span data-ttu-id="e45a9-118">Nesne kimliği ' 155a5c10-93a9-4941-a0df-96vseç83ab5ab24 ' olan kullanıcıyı ve bu kullanıcının görünen adını ' Yenisdisplayname ' olarak güncelleştirmek için Update-AzADUser cmdlet 'ine sahip olan kullanıcıyı alır.</span><span class="sxs-lookup"><span data-stu-id="e45a9-118">Gets the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' and pipes that to the Update-AzADUser cmdlet to update the display name of that user to 'MyNewDisplayName'.</span></span>

## <span data-ttu-id="e45a9-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e45a9-119">PARAMETERS</span></span>

### <span data-ttu-id="e45a9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e45a9-120">-DefaultProfile</span></span>
<span data-ttu-id="e45a9-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e45a9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e45a9-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e45a9-122">-DisplayName</span></span>
<span data-ttu-id="e45a9-123">Kullanıcı için yeni görünen ad.</span><span class="sxs-lookup"><span data-stu-id="e45a9-123">New display name for the user.</span></span>

```yaml
Type: System.String
Parameter Sets: UPNOrObjectIdParameterSet, UPNParameterSet, ObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e45a9-124">-EnableAccount</span><span class="sxs-lookup"><span data-stu-id="e45a9-124">-EnableAccount</span></span>
<span data-ttu-id="e45a9-125">hesabı etkinleştirmek için doğru; Aksi takdirde, false.</span><span class="sxs-lookup"><span data-stu-id="e45a9-125">true for enabling the account; otherwise, false.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: UPNOrObjectIdParameterSet, UPNParameterSet, ObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e45a9-126">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="e45a9-126">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="e45a9-127">Kullanıcının sonraki başarılı oturum açma durumunda parolayı değiştirmesi gerekiyorsa belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="e45a9-127">It must be specified if the user should change the password on the next successful login.</span></span>
<span data-ttu-id="e45a9-128">Yalnızca parola güncelleştirildiyse geçerli değildir.</span><span class="sxs-lookup"><span data-stu-id="e45a9-128">Only valid if password is updated otherwise it will be ignored.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e45a9-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e45a9-129">-InputObject</span></span>
<span data-ttu-id="e45a9-130">Güncelleştirilecek kullanıcıyı temsil eden nesne.</span><span class="sxs-lookup"><span data-stu-id="e45a9-130">The object representing the user to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e45a9-131">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="e45a9-131">-ObjectId</span></span>
<span data-ttu-id="e45a9-132">Güncelleştirilecek kullanıcının nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="e45a9-132">The object id of the user to be updated.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e45a9-133">-Parola</span><span class="sxs-lookup"><span data-stu-id="e45a9-133">-Password</span></span>
<span data-ttu-id="e45a9-134">Kullanıcı için yeni parola.</span><span class="sxs-lookup"><span data-stu-id="e45a9-134">New password for the user.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: UPNOrObjectIdParameterSet, UPNParameterSet, ObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e45a9-135">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="e45a9-135">-UPNOrObjectId</span></span>
<span data-ttu-id="e45a9-136">Güncelleştirilecek kullanıcının Kullanıcı asıl adı veya nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="e45a9-136">The user principal name or object id of the user to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: UPNOrObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e45a9-137">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="e45a9-137">-UserPrincipalName</span></span>
<span data-ttu-id="e45a9-138">Güncelleştirilecek kullanıcının Kullanıcı asıl adı.</span><span class="sxs-lookup"><span data-stu-id="e45a9-138">The user principal name of the user to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: UPNParameterSet
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e45a9-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="e45a9-139">-Confirm</span></span>
<span data-ttu-id="e45a9-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e45a9-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e45a9-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e45a9-141">-WhatIf</span></span>
<span data-ttu-id="e45a9-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e45a9-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e45a9-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e45a9-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e45a9-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e45a9-144">CommonParameters</span></span>
<span data-ttu-id="e45a9-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e45a9-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e45a9-146">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e45a9-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e45a9-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e45a9-147">INPUTS</span></span>

### <span data-ttu-id="e45a9-148">System. String</span><span class="sxs-lookup"><span data-stu-id="e45a9-148">System.String</span></span>

### <span data-ttu-id="e45a9-149">System. Guid</span><span class="sxs-lookup"><span data-stu-id="e45a9-149">System.Guid</span></span>

### <span data-ttu-id="e45a9-150">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="e45a9-150">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>
<span data-ttu-id="e45a9-151">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e45a9-151">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="e45a9-152">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e45a9-152">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="e45a9-153">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="e45a9-153">System.Security.SecureString</span></span>

## <span data-ttu-id="e45a9-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e45a9-154">OUTPUTS</span></span>

### <span data-ttu-id="e45a9-155">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="e45a9-155">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="e45a9-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e45a9-156">NOTES</span></span>

## <span data-ttu-id="e45a9-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e45a9-157">RELATED LINKS</span></span>
