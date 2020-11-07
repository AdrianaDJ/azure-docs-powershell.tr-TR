---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 9F9B2691-BB3F-4644-BD95-6D74777D1E99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADUser.md
ms.openlocfilehash: 1b863b0bc9cb90caca4d7431ec6835cb75836609
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763809"
---
# <span data-ttu-id="1c692-101">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="1c692-101">Remove-AzureRmADUser</span></span>

## <span data-ttu-id="1c692-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c692-102">SYNOPSIS</span></span>
<span data-ttu-id="1c692-103">Active Directory kullanıcısını siler.</span><span class="sxs-lookup"><span data-stu-id="1c692-103">Deletes an active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c692-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1c692-104">SYNTAX</span></span>

### <span data-ttu-id="1c692-105">Upnorobjectivseçparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1c692-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Remove-AzureRmADUser -UPNOrObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c692-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c692-106">UPNParameterSet</span></span>
```
Remove-AzureRmADUser -UserPrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c692-107">NesneKimliği</span><span class="sxs-lookup"><span data-stu-id="1c692-107">ObjectIdParameterSet</span></span>
```
Remove-AzureRmADUser -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c692-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1c692-108">DisplayNameParameterSet</span></span>
```
Remove-AzureRmADUser -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c692-109">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="1c692-109">InputObjectParameterSet</span></span>
```
Remove-AzureRmADUser -InputObject <PSADUser> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c692-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="1c692-110">DESCRIPTION</span></span>
<span data-ttu-id="1c692-111">Active Directory kullanıcısını (iş/okul hesabı, ayrıca org-ID olarak da bilinir) siler.</span><span class="sxs-lookup"><span data-stu-id="1c692-111">Deletes an active directory user (work/school account also popularly known as org-id).</span></span>

## <span data-ttu-id="1c692-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1c692-112">EXAMPLES</span></span>

### <span data-ttu-id="1c692-113">Örnek 1-kullanıcıyı Kullanıcı asıl adına göre kaldırma</span><span class="sxs-lookup"><span data-stu-id="1c692-113">Example 1 - Remove a user by user principal name</span></span>

```
PS C:\> Remove-AzureRmADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="1c692-114">Kullanıcıyı kiracının Kullanıcı asıl adıyla kaldırır foo@domain.com .</span><span class="sxs-lookup"><span data-stu-id="1c692-114">Removes the user with user principal name "foo@domain.com" from the tenant.</span></span>

### <span data-ttu-id="1c692-115">Örnek 2-nesne kimliğiyle bir kullanıcıyı kaldırma</span><span class="sxs-lookup"><span data-stu-id="1c692-115">Example 2 - Remove a user by object id</span></span>

```
PS C:\> Remove-AzureRmADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69
```

<span data-ttu-id="1c692-116">Nesne kimliği ' 7a9582cf-88c4-4319-842b-7a5d60967a69 ' olan kullanıcıyı kiracıdan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1c692-116">Removes the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' from the tenant.</span></span>

### <span data-ttu-id="1c692-117">Örnek 3-boruları kullanarak kullanıcıyı kaldırın</span><span class="sxs-lookup"><span data-stu-id="1c692-117">Example 3 - Remove a user by piping</span></span>

```
PS C:\> Get-AzureRmADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69 | Remove-AzureRmADUser
```

<span data-ttu-id="1c692-118">Nesne kimliği ' 7a9582cf-88c4-4319-842b-7a5d60967a69 ' ve kanalları kiracıyı kaldırmak için Remove-AzureRmADUser cmdlet 'ine sahip kullanıcıyı alır.</span><span class="sxs-lookup"><span data-stu-id="1c692-118">Gets the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' and pipes that to the Remove-AzureRmADUser cmdlet to remove the user from the tenant.</span></span>

## <span data-ttu-id="1c692-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1c692-119">PARAMETERS</span></span>

### <span data-ttu-id="1c692-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c692-120">-DefaultProfile</span></span>
<span data-ttu-id="1c692-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="1c692-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c692-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1c692-122">-DisplayName</span></span>
<span data-ttu-id="1c692-123">Silinecek kullanıcının görünen adı.</span><span class="sxs-lookup"><span data-stu-id="1c692-123">The display name of the user to be deleted.</span></span>

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

### <span data-ttu-id="1c692-124">-Force</span><span class="sxs-lookup"><span data-stu-id="1c692-124">-Force</span></span>
<span data-ttu-id="1c692-125">Belirtilmişse, kullanıcıyı silme konusunda onay vermez.</span><span class="sxs-lookup"><span data-stu-id="1c692-125">If specified, doesn't ask for confirmation for deleting the user.</span></span>

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

### <span data-ttu-id="1c692-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c692-126">-InputObject</span></span>
<span data-ttu-id="1c692-127">Silinecek kullanıcı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="1c692-127">The user object to be deleted.</span></span>

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

### <span data-ttu-id="1c692-128">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="1c692-128">-ObjectId</span></span>
<span data-ttu-id="1c692-129">Silinecek kullanıcının nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="1c692-129">The object id of the user to be deleted.</span></span>

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

### <span data-ttu-id="1c692-130">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="1c692-130">-PassThru</span></span>
<span data-ttu-id="1c692-131">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="1c692-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="1c692-132">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="1c692-132">-UPNOrObjectId</span></span>
<span data-ttu-id="1c692-133">Silinecek kullanıcının Kullanıcı asıl adı veya ObjectID.</span><span class="sxs-lookup"><span data-stu-id="1c692-133">The user principal name or the objectId of the user to be deleted.</span></span>

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

### <span data-ttu-id="1c692-134">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="1c692-134">-UserPrincipalName</span></span>
<span data-ttu-id="1c692-135">Silinecek kullanıcının Kullanıcı asıl adı.</span><span class="sxs-lookup"><span data-stu-id="1c692-135">The user principal name of the user to be deleted.</span></span>

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

### <span data-ttu-id="1c692-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="1c692-136">-Confirm</span></span>
<span data-ttu-id="1c692-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1c692-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c692-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c692-138">-WhatIf</span></span>
<span data-ttu-id="1c692-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1c692-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c692-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1c692-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c692-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c692-141">CommonParameters</span></span>
<span data-ttu-id="1c692-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1c692-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c692-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c692-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c692-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1c692-144">INPUTS</span></span>

### <span data-ttu-id="1c692-145">System. String</span><span class="sxs-lookup"><span data-stu-id="1c692-145">System.String</span></span>

### <span data-ttu-id="1c692-146">System. Guid</span><span class="sxs-lookup"><span data-stu-id="1c692-146">System.Guid</span></span>

### <span data-ttu-id="1c692-147">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="1c692-147">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>
<span data-ttu-id="1c692-148">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1c692-148">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="1c692-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1c692-149">OUTPUTS</span></span>

### <span data-ttu-id="1c692-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1c692-150">System.Boolean</span></span>

## <span data-ttu-id="1c692-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1c692-151">NOTES</span></span>

## <span data-ttu-id="1c692-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1c692-152">RELATED LINKS</span></span>

[<span data-ttu-id="1c692-153">Yeni-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="1c692-153">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="1c692-154">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="1c692-154">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="1c692-155">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="1c692-155">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

