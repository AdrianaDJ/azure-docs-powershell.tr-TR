---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 9F9B2691-BB3F-4644-BD95-6D74777D1E99
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADUser.md
ms.openlocfilehash: 2dc9a0d3d41ca1bccb131e92cf514fd2f814943b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933323"
---
# <span data-ttu-id="11081-101">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="11081-101">Remove-AzADUser</span></span>

## <span data-ttu-id="11081-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11081-102">SYNOPSIS</span></span>
<span data-ttu-id="11081-103">Active Directory kullanıcısını siler.</span><span class="sxs-lookup"><span data-stu-id="11081-103">Deletes an active directory user.</span></span>

## <span data-ttu-id="11081-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="11081-104">SYNTAX</span></span>

### <span data-ttu-id="11081-105">Upnorobjectivseçparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="11081-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Remove-AzADUser -UPNOrObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11081-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="11081-106">UPNParameterSet</span></span>
```
Remove-AzADUser -UserPrincipalName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11081-107">NesneKimliği</span><span class="sxs-lookup"><span data-stu-id="11081-107">ObjectIdParameterSet</span></span>
```
Remove-AzADUser -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11081-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="11081-108">DisplayNameParameterSet</span></span>
```
Remove-AzADUser -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11081-109">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="11081-109">InputObjectParameterSet</span></span>
```
Remove-AzADUser -InputObject <PSADUser> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11081-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="11081-110">DESCRIPTION</span></span>
<span data-ttu-id="11081-111">Active Directory kullanıcısını (iş/okul hesabı, ayrıca org-ID olarak da bilinir) siler.</span><span class="sxs-lookup"><span data-stu-id="11081-111">Deletes an active directory user (work/school account also popularly known as org-id).</span></span>

## <span data-ttu-id="11081-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="11081-112">EXAMPLES</span></span>

### <span data-ttu-id="11081-113">Örnek 1-kullanıcıyı Kullanıcı asıl adına göre kaldırma</span><span class="sxs-lookup"><span data-stu-id="11081-113">Example 1 - Remove a user by user principal name</span></span>

```
PS C:\> Remove-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="11081-114">Kullanıcıyı kiracının Kullanıcı asıl adıyla kaldırır foo@domain.com .</span><span class="sxs-lookup"><span data-stu-id="11081-114">Removes the user with user principal name "foo@domain.com" from the tenant.</span></span>

### <span data-ttu-id="11081-115">Örnek 2-nesne kimliğiyle bir kullanıcıyı kaldırma</span><span class="sxs-lookup"><span data-stu-id="11081-115">Example 2 - Remove a user by object id</span></span>

```
PS C:\> Remove-AzADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69
```

<span data-ttu-id="11081-116">Nesne kimliği ' 7a9582cf-88c4-4319-842b-7a5d60967a69 ' olan kullanıcıyı kiracıdan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="11081-116">Removes the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' from the tenant.</span></span>

### <span data-ttu-id="11081-117">Örnek 3-boruları kullanarak kullanıcıyı kaldırın</span><span class="sxs-lookup"><span data-stu-id="11081-117">Example 3 - Remove a user by piping</span></span>

```
PS C:\> Get-AzADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69 | Remove-AzADUser
```

<span data-ttu-id="11081-118">Nesne kimliği ' 7a9582cf-88c4-4319-842b-7a5d60967a69 ' ve kanalları kiracıyı kaldırmak için Remove-AzADUser cmdlet 'ine sahip kullanıcıyı alır.</span><span class="sxs-lookup"><span data-stu-id="11081-118">Gets the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' and pipes that to the Remove-AzADUser cmdlet to remove the user from the tenant.</span></span>

## <span data-ttu-id="11081-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="11081-119">PARAMETERS</span></span>

### <span data-ttu-id="11081-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11081-120">-DefaultProfile</span></span>
<span data-ttu-id="11081-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="11081-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11081-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="11081-122">-DisplayName</span></span>
<span data-ttu-id="11081-123">Silinecek kullanıcının görünen adı.</span><span class="sxs-lookup"><span data-stu-id="11081-123">The display name of the user to be deleted.</span></span>

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

### <span data-ttu-id="11081-124">-Force</span><span class="sxs-lookup"><span data-stu-id="11081-124">-Force</span></span>
<span data-ttu-id="11081-125">Belirtilmişse, kullanıcıyı silme konusunda onay vermez.</span><span class="sxs-lookup"><span data-stu-id="11081-125">If specified, doesn't ask for confirmation for deleting the user.</span></span>

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

### <span data-ttu-id="11081-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11081-126">-InputObject</span></span>
<span data-ttu-id="11081-127">Silinecek kullanıcı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="11081-127">The user object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADUser
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11081-128">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="11081-128">-ObjectId</span></span>
<span data-ttu-id="11081-129">Silinecek kullanıcının nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="11081-129">The object id of the user to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11081-130">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="11081-130">-PassThru</span></span>
<span data-ttu-id="11081-131">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="11081-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="11081-132">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="11081-132">-UPNOrObjectId</span></span>
<span data-ttu-id="11081-133">Silinecek kullanıcının Kullanıcı asıl adı veya ObjectID.</span><span class="sxs-lookup"><span data-stu-id="11081-133">The user principal name or the objectId of the user to be deleted.</span></span>

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

### <span data-ttu-id="11081-134">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="11081-134">-UserPrincipalName</span></span>
<span data-ttu-id="11081-135">Silinecek kullanıcının Kullanıcı asıl adı.</span><span class="sxs-lookup"><span data-stu-id="11081-135">The user principal name of the user to be deleted.</span></span>

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

### <span data-ttu-id="11081-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="11081-136">-Confirm</span></span>
<span data-ttu-id="11081-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="11081-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11081-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11081-138">-WhatIf</span></span>
<span data-ttu-id="11081-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="11081-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11081-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="11081-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11081-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11081-141">CommonParameters</span></span>
<span data-ttu-id="11081-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="11081-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11081-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11081-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11081-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="11081-144">INPUTS</span></span>

### <span data-ttu-id="11081-145">System. String</span><span class="sxs-lookup"><span data-stu-id="11081-145">System.String</span></span>

### <span data-ttu-id="11081-146">Microsoft. Azure. Commands. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="11081-146">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="11081-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="11081-147">OUTPUTS</span></span>

### <span data-ttu-id="11081-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="11081-148">System.Boolean</span></span>

## <span data-ttu-id="11081-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="11081-149">NOTES</span></span>

## <span data-ttu-id="11081-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="11081-150">RELATED LINKS</span></span>

[<span data-ttu-id="11081-151">Yeni-AzADUser</span><span class="sxs-lookup"><span data-stu-id="11081-151">New-AzADUser</span></span>](./New-AzADUser.md)

[<span data-ttu-id="11081-152">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="11081-152">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="11081-153">Set-AzADUser</span><span class="sxs-lookup"><span data-stu-id="11081-153">Set-AzADUser</span></span>](./Set-AzADUser.md)

