---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 638B2BF6-23F8-4038-B20B-1CFABFDBF5D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUser.md
ms.openlocfilehash: 1734eeb341d850f61fa3d5e930cabc26a4060de6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751139"
---
# <span data-ttu-id="83f80-101">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="83f80-101">Get-AzApiManagementUser</span></span>

## <span data-ttu-id="83f80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83f80-102">SYNOPSIS</span></span>
<span data-ttu-id="83f80-103">Bir kullanıcıyı veya kullanıcıları alır.</span><span class="sxs-lookup"><span data-stu-id="83f80-103">Gets a user or users.</span></span>

## <span data-ttu-id="83f80-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="83f80-104">SYNTAX</span></span>

### <span data-ttu-id="83f80-105">GeAllUsers (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="83f80-105">GeAllUsers (Default)</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="83f80-106">Getbyuserıd</span><span class="sxs-lookup"><span data-stu-id="83f80-106">GetByUserId</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83f80-107">GetByUser</span><span class="sxs-lookup"><span data-stu-id="83f80-107">GetByUser</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-FirstName <String>] [-LastName <String>]
 [-State <PsApiManagementUserState>] [-Email <String>] [-GroupId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83f80-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="83f80-108">DESCRIPTION</span></span>
<span data-ttu-id="83f80-109">**Get-Azapsananagementuser** cmdlet 'i belirtilen kullanıcıyı veya herhangi bir Kullanıcı belirtilmemişse tüm kullanıcıları alır.</span><span class="sxs-lookup"><span data-stu-id="83f80-109">The **Get-AzApiManagementUser** cmdlet gets a specified user, or all users, if no user is specified.</span></span>

## <span data-ttu-id="83f80-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="83f80-110">EXAMPLES</span></span>

### <span data-ttu-id="83f80-111">Örnek 1: tüm kullanıcıları alma</span><span class="sxs-lookup"><span data-stu-id="83f80-111">Example 1: Get all users</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext
```

<span data-ttu-id="83f80-112">Bu komut tüm kullanıcıları alır.</span><span class="sxs-lookup"><span data-stu-id="83f80-112">This command gets all users.</span></span>

### <span data-ttu-id="83f80-113">Örnek 2: KIMLIĞE göre bir Kullanıcı alma</span><span class="sxs-lookup"><span data-stu-id="83f80-113">Example 2: Get a user by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="83f80-114">Bu komut bir kullanıcıyı KIMLIĞE göre alır.</span><span class="sxs-lookup"><span data-stu-id="83f80-114">This command gets a user by ID.</span></span>

### <span data-ttu-id="83f80-115">Örnek: kullanıcıları soyadına göre alma</span><span class="sxs-lookup"><span data-stu-id="83f80-115">Example: Get users by last name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -LastName "Fuller"
```

<span data-ttu-id="83f80-116">Bu komut, belirli bir soyadınız olan kullanıcıları alır.</span><span class="sxs-lookup"><span data-stu-id="83f80-116">This command gets users that have a specified last name, Fuller.</span></span>

### <span data-ttu-id="83f80-117">Örnek 4: e-posta adresine göre Kullanıcı alma</span><span class="sxs-lookup"><span data-stu-id="83f80-117">Example 4: Get a user by email address</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -Email "user@contoso.com"
```

<span data-ttu-id="83f80-118">Bu komut, belirtilen e-posta adresine sahip kullanıcıyı alır.</span><span class="sxs-lookup"><span data-stu-id="83f80-118">This command gets the user that has the specified email address.</span></span>

### <span data-ttu-id="83f80-119">Örnek 5: Grup içindeki tüm kullanıcıları alma</span><span class="sxs-lookup"><span data-stu-id="83f80-119">Example 5: Get all users within a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -GroupId "0001"
```

<span data-ttu-id="83f80-120">Bu komut belirtilen gruptaki tüm kullanıcıları alır.</span><span class="sxs-lookup"><span data-stu-id="83f80-120">This command gets all users within the specified group.</span></span>

## <span data-ttu-id="83f80-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="83f80-121">PARAMETERS</span></span>

### <span data-ttu-id="83f80-122">-Context</span><span class="sxs-lookup"><span data-stu-id="83f80-122">-Context</span></span>
<span data-ttu-id="83f80-123">**Psapsananagementcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="83f80-123">Specifies an instance of **PsApiManagementContext**.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83f80-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83f80-124">-DefaultProfile</span></span>
<span data-ttu-id="83f80-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="83f80-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83f80-126">-E-posta</span><span class="sxs-lookup"><span data-stu-id="83f80-126">-Email</span></span>
<span data-ttu-id="83f80-127">Kullanıcının e-posta adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="83f80-127">Specifies the email address of the user.</span></span>
<span data-ttu-id="83f80-128">Bu parametre belirtilmişse, bu cmdlet bir kullanıcıyı e-posta ile bulur.</span><span class="sxs-lookup"><span data-stu-id="83f80-128">If this parameter is specified, this cmdlet finds a user by email.</span></span>
<span data-ttu-id="83f80-129">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="83f80-129">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83f80-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="83f80-130">-FirstName</span></span>
<span data-ttu-id="83f80-131">Kullanıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="83f80-131">Specifies the first name of the user.</span></span>
<span data-ttu-id="83f80-132">Bu parametre belirtilmişse, bu cmdlet bir kullanıcıyı adıyla bulur.</span><span class="sxs-lookup"><span data-stu-id="83f80-132">If this parameter is specified, this cmdlet finds a user by first name.</span></span>
<span data-ttu-id="83f80-133">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="83f80-133">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83f80-134">-GroupID</span><span class="sxs-lookup"><span data-stu-id="83f80-134">-GroupId</span></span>
<span data-ttu-id="83f80-135">Grup tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="83f80-135">Specifies the group identifier.</span></span>
<span data-ttu-id="83f80-136">Belirtilmişse, bu cmdlet belirtilen gruptaki tüm kullanıcıları bulur.</span><span class="sxs-lookup"><span data-stu-id="83f80-136">If specified, this cmdlet finds all users within the specified group.</span></span>
<span data-ttu-id="83f80-137">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="83f80-137">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83f80-138">-LastName</span><span class="sxs-lookup"><span data-stu-id="83f80-138">-LastName</span></span>
<span data-ttu-id="83f80-139">Kullanıcının soyadını belirtir.</span><span class="sxs-lookup"><span data-stu-id="83f80-139">Specifies the last name of a user.</span></span>
<span data-ttu-id="83f80-140">Belirtilmişse, bu cmdlet kullanıcıları soyadına göre bulur.</span><span class="sxs-lookup"><span data-stu-id="83f80-140">If specified, this cmdlet finds users by last name.</span></span>
<span data-ttu-id="83f80-141">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="83f80-141">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUser
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83f80-142">Durumlu</span><span class="sxs-lookup"><span data-stu-id="83f80-142">-State</span></span>
<span data-ttu-id="83f80-143">Kullanıcı durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="83f80-143">Specifies the user state.</span></span>
<span data-ttu-id="83f80-144">Belirtilmişse bu cmdlet bu durumda kullanıcıları bulur.</span><span class="sxs-lookup"><span data-stu-id="83f80-144">If specified, this cmdlet finds users in this state.</span></span>
<span data-ttu-id="83f80-145">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="83f80-145">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: GetByUser
Aliases:
Accepted values: Active, Blocked, Deleted, Pending

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83f80-146">-UserID</span><span class="sxs-lookup"><span data-stu-id="83f80-146">-UserId</span></span>
<span data-ttu-id="83f80-147">Bir kullanıcı KIMLIĞI belirtir.</span><span class="sxs-lookup"><span data-stu-id="83f80-147">Specifies a user ID.</span></span>
<span data-ttu-id="83f80-148">Belirtilmişse, bu cmdlet kullanıcıyı bu tanımlayıcıyla bulur.</span><span class="sxs-lookup"><span data-stu-id="83f80-148">If specified, this cmdlet finds the user by this identifier.</span></span>
<span data-ttu-id="83f80-149">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="83f80-149">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUserId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83f80-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83f80-150">CommonParameters</span></span>
<span data-ttu-id="83f80-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="83f80-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83f80-152">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83f80-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83f80-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="83f80-153">INPUTS</span></span>

### <span data-ttu-id="83f80-154">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="83f80-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="83f80-155">System. String</span><span class="sxs-lookup"><span data-stu-id="83f80-155">System.String</span></span>

### <span data-ttu-id="83f80-156">System. Nullable ' 1 [[Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementuserstate, Microsoft. Azure. PowerShell. cmdlet</span><span class="sxs-lookup"><span data-stu-id="83f80-156">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="83f80-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="83f80-157">OUTPUTS</span></span>

### <span data-ttu-id="83f80-158">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementuser</span><span class="sxs-lookup"><span data-stu-id="83f80-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="83f80-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="83f80-159">NOTES</span></span>

## <span data-ttu-id="83f80-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="83f80-160">RELATED LINKS</span></span>

[<span data-ttu-id="83f80-161">Yeni-Azsız Kullanıcı</span><span class="sxs-lookup"><span data-stu-id="83f80-161">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="83f80-162">Remove-Azapsananagementuser</span><span class="sxs-lookup"><span data-stu-id="83f80-162">Remove-AzApiManagementUser</span></span>](./Remove-AzApiManagementUser.md)

[<span data-ttu-id="83f80-163">Set-Azapsananagementuser</span><span class="sxs-lookup"><span data-stu-id="83f80-163">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


