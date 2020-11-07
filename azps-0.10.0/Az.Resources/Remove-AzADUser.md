---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 9F9B2691-BB3F-4644-BD95-6D74777D1E99
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzADUser.md
ms.openlocfilehash: 091f54b69cd713d93def4c727181f9c8e7d5b0d6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936358"
---
# <span data-ttu-id="373ef-101">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="373ef-101">Remove-AzADUser</span></span>

## <span data-ttu-id="373ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="373ef-102">SYNOPSIS</span></span>
<span data-ttu-id="373ef-103">Active Directory kullanıcısını siler.</span><span class="sxs-lookup"><span data-stu-id="373ef-103">Deletes an active directory user.</span></span>

## <span data-ttu-id="373ef-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="373ef-104">SYNTAX</span></span>

### <span data-ttu-id="373ef-105">Upnorobjectivseçparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="373ef-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Remove-AzADUser -UPNOrObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="373ef-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="373ef-106">UPNParameterSet</span></span>
```
Remove-AzADUser -UserPrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="373ef-107">NesneKimliği</span><span class="sxs-lookup"><span data-stu-id="373ef-107">ObjectIdParameterSet</span></span>
```
Remove-AzADUser -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="373ef-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="373ef-108">DisplayNameParameterSet</span></span>
```
Remove-AzADUser -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="373ef-109">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="373ef-109">InputObjectParameterSet</span></span>
```
Remove-AzADUser -InputObject <PSADUser> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="373ef-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="373ef-110">DESCRIPTION</span></span>
<span data-ttu-id="373ef-111">Active Directory kullanıcısını (iş/okul hesabı, ayrıca org-ID olarak da bilinir) siler.</span><span class="sxs-lookup"><span data-stu-id="373ef-111">Deletes an active directory user (work/school account also popularly known as org-id).</span></span>

## <span data-ttu-id="373ef-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="373ef-112">EXAMPLES</span></span>

### <span data-ttu-id="373ef-113">Örnek 1-kullanıcıyı Kullanıcı asıl adına göre kaldırma</span><span class="sxs-lookup"><span data-stu-id="373ef-113">Example 1 - Remove a user by user principal name</span></span>

```
PS C:\> Remove-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="373ef-114">Kullanıcıyı kiracının Kullanıcı asıl adıyla kaldırır foo@domain.com .</span><span class="sxs-lookup"><span data-stu-id="373ef-114">Removes the user with user principal name "foo@domain.com" from the tenant.</span></span>

### <span data-ttu-id="373ef-115">Örnek 2-nesne kimliğiyle bir kullanıcıyı kaldırma</span><span class="sxs-lookup"><span data-stu-id="373ef-115">Example 2 - Remove a user by object id</span></span>

```
PS C:\> Remove-AzADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69
```

<span data-ttu-id="373ef-116">Nesne kimliği ' 7a9582cf-88c4-4319-842b-7a5d60967a69 ' olan kullanıcıyı kiracıdan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="373ef-116">Removes the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' from the tenant.</span></span>

### <span data-ttu-id="373ef-117">Örnek 3-boruları kullanarak kullanıcıyı kaldırın</span><span class="sxs-lookup"><span data-stu-id="373ef-117">Example 3 - Remove a user by piping</span></span>

```
PS C:\> Get-AzADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69 | Remove-AzADUser
```

<span data-ttu-id="373ef-118">Nesne kimliği ' 7a9582cf-88c4-4319-842b-7a5d60967a69 ' ve kanalları kiracıyı kaldırmak için Remove-AzADUser cmdlet 'ine sahip kullanıcıyı alır.</span><span class="sxs-lookup"><span data-stu-id="373ef-118">Gets the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' and pipes that to the Remove-AzADUser cmdlet to remove the user from the tenant.</span></span>

## <span data-ttu-id="373ef-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="373ef-119">PARAMETERS</span></span>

### <span data-ttu-id="373ef-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="373ef-120">-DefaultProfile</span></span>
<span data-ttu-id="373ef-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="373ef-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="373ef-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="373ef-122">-DisplayName</span></span>
<span data-ttu-id="373ef-123">Silinecek kullanıcının görünen adı.</span><span class="sxs-lookup"><span data-stu-id="373ef-123">The display name of the user to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="373ef-124">-Force</span><span class="sxs-lookup"><span data-stu-id="373ef-124">-Force</span></span>
<span data-ttu-id="373ef-125">Belirtilmişse, kullanıcıyı silme konusunda onay vermez.</span><span class="sxs-lookup"><span data-stu-id="373ef-125">If specified, doesn't ask for confirmation for deleting the user.</span></span>

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

### <span data-ttu-id="373ef-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="373ef-126">-InputObject</span></span>
<span data-ttu-id="373ef-127">Silinecek kullanıcı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="373ef-127">The user object to be deleted.</span></span>

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

### <span data-ttu-id="373ef-128">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="373ef-128">-ObjectId</span></span>
<span data-ttu-id="373ef-129">Silinecek kullanıcının nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="373ef-129">The object id of the user to be deleted.</span></span>

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

### <span data-ttu-id="373ef-130">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="373ef-130">-PassThru</span></span>
<span data-ttu-id="373ef-131">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="373ef-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="373ef-132">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="373ef-132">-UPNOrObjectId</span></span>
<span data-ttu-id="373ef-133">Silinecek kullanıcının Kullanıcı asıl adı veya ObjectID.</span><span class="sxs-lookup"><span data-stu-id="373ef-133">The user principal name or the objectId of the user to be deleted.</span></span>

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

### <span data-ttu-id="373ef-134">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="373ef-134">-UserPrincipalName</span></span>
<span data-ttu-id="373ef-135">Silinecek kullanıcının Kullanıcı asıl adı.</span><span class="sxs-lookup"><span data-stu-id="373ef-135">The user principal name of the user to be deleted.</span></span>

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

### <span data-ttu-id="373ef-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="373ef-136">-Confirm</span></span>
<span data-ttu-id="373ef-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="373ef-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="373ef-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="373ef-138">-WhatIf</span></span>
<span data-ttu-id="373ef-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="373ef-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="373ef-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="373ef-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="373ef-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="373ef-141">CommonParameters</span></span>
<span data-ttu-id="373ef-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="373ef-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="373ef-143">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="373ef-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="373ef-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="373ef-144">INPUTS</span></span>

### <span data-ttu-id="373ef-145">System. String</span><span class="sxs-lookup"><span data-stu-id="373ef-145">System.String</span></span>

### <span data-ttu-id="373ef-146">System. Guid</span><span class="sxs-lookup"><span data-stu-id="373ef-146">System.Guid</span></span>

### <span data-ttu-id="373ef-147">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="373ef-147">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>
<span data-ttu-id="373ef-148">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="373ef-148">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="373ef-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="373ef-149">OUTPUTS</span></span>

### <span data-ttu-id="373ef-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="373ef-150">System.Boolean</span></span>

## <span data-ttu-id="373ef-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="373ef-151">NOTES</span></span>

## <span data-ttu-id="373ef-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="373ef-152">RELATED LINKS</span></span>

[<span data-ttu-id="373ef-153">Yeni-AzADUser</span><span class="sxs-lookup"><span data-stu-id="373ef-153">New-AzADUser</span></span>](./New-AzADUser.md)

[<span data-ttu-id="373ef-154">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="373ef-154">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="373ef-155">Set-AzADUser</span><span class="sxs-lookup"><span data-stu-id="373ef-155">Set-AzADUser</span></span>](./Set-AzADUser.md)

