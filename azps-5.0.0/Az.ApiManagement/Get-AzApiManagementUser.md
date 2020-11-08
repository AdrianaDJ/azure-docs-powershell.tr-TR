---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 638B2BF6-23F8-4038-B20B-1CFABFDBF5D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUser.md
ms.openlocfilehash: 44f351870e97d227484bd09be1e75b8cb19ac723
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276465"
---
# <span data-ttu-id="255ca-101">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="255ca-101">Get-AzApiManagementUser</span></span>

## <span data-ttu-id="255ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="255ca-102">SYNOPSIS</span></span>
<span data-ttu-id="255ca-103">Bir kullanıcıyı veya kullanıcıları alır.</span><span class="sxs-lookup"><span data-stu-id="255ca-103">Gets a user or users.</span></span>

## <span data-ttu-id="255ca-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="255ca-104">SYNTAX</span></span>

### <span data-ttu-id="255ca-105">GeAllUsers (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="255ca-105">GeAllUsers (Default)</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="255ca-106">Getbyuserıd</span><span class="sxs-lookup"><span data-stu-id="255ca-106">GetByUserId</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="255ca-107">GetByUser</span><span class="sxs-lookup"><span data-stu-id="255ca-107">GetByUser</span></span>
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-FirstName <String>] [-LastName <String>]
 [-State <PsApiManagementUserState>] [-Email <String>] [-GroupId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="255ca-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="255ca-108">DESCRIPTION</span></span>
<span data-ttu-id="255ca-109">**Get-Azapsananagementuser** cmdlet 'i belirtilen kullanıcıyı veya herhangi bir Kullanıcı belirtilmemişse tüm kullanıcıları alır.</span><span class="sxs-lookup"><span data-stu-id="255ca-109">The **Get-AzApiManagementUser** cmdlet gets a specified user, or all users, if no user is specified.</span></span>

## <span data-ttu-id="255ca-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="255ca-110">EXAMPLES</span></span>

### <span data-ttu-id="255ca-111">Örnek 1: tüm kullanıcıları alma</span><span class="sxs-lookup"><span data-stu-id="255ca-111">Example 1: Get all users</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext
```

<span data-ttu-id="255ca-112">Bu komut tüm kullanıcıları alır.</span><span class="sxs-lookup"><span data-stu-id="255ca-112">This command gets all users.</span></span>

### <span data-ttu-id="255ca-113">Örnek 2: KIMLIĞE göre bir Kullanıcı alma</span><span class="sxs-lookup"><span data-stu-id="255ca-113">Example 2: Get a user by ID</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="255ca-114">Bu komut bir kullanıcıyı KIMLIĞE göre alır.</span><span class="sxs-lookup"><span data-stu-id="255ca-114">This command gets a user by ID.</span></span>

### <span data-ttu-id="255ca-115">Örnek 3: soyadlarına göre kullanıcıları alma</span><span class="sxs-lookup"><span data-stu-id="255ca-115">Example 3: Get users by last name</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -LastName "Fuller"
```

<span data-ttu-id="255ca-116">Bu komut, belirli bir soyadınız olan kullanıcıları alır.</span><span class="sxs-lookup"><span data-stu-id="255ca-116">This command gets users that have a specified last name, Fuller.</span></span>

### <span data-ttu-id="255ca-117">Örnek 4: e-posta adresine göre Kullanıcı alma</span><span class="sxs-lookup"><span data-stu-id="255ca-117">Example 4: Get a user by email address</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -Email "user@contoso.com"
```

<span data-ttu-id="255ca-118">Bu komut, belirtilen e-posta adresine sahip kullanıcıyı alır.</span><span class="sxs-lookup"><span data-stu-id="255ca-118">This command gets the user that has the specified email address.</span></span>

### <span data-ttu-id="255ca-119">Örnek 5: Grup içindeki tüm kullanıcıları alma</span><span class="sxs-lookup"><span data-stu-id="255ca-119">Example 5: Get all users within a group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -GroupId "0001"
```

<span data-ttu-id="255ca-120">Bu komut belirtilen gruptaki tüm kullanıcıları alır.</span><span class="sxs-lookup"><span data-stu-id="255ca-120">This command gets all users within the specified group.</span></span>

## <span data-ttu-id="255ca-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="255ca-121">PARAMETERS</span></span>

### <span data-ttu-id="255ca-122">-Context</span><span class="sxs-lookup"><span data-stu-id="255ca-122">-Context</span></span>
<span data-ttu-id="255ca-123">**Psapsananagementcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="255ca-123">Specifies an instance of **PsApiManagementContext**.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="255ca-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="255ca-124">-DefaultProfile</span></span>
<span data-ttu-id="255ca-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="255ca-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="255ca-126">-E-posta</span><span class="sxs-lookup"><span data-stu-id="255ca-126">-Email</span></span>
<span data-ttu-id="255ca-127">Kullanıcının e-posta adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="255ca-127">Specifies the email address of the user.</span></span>
<span data-ttu-id="255ca-128">Bu parametre belirtilmişse, bu cmdlet bir kullanıcıyı e-posta ile bulur.</span><span class="sxs-lookup"><span data-stu-id="255ca-128">If this parameter is specified, this cmdlet finds a user by email.</span></span>
<span data-ttu-id="255ca-129">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="255ca-129">This parameter is optional.</span></span>

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

### <span data-ttu-id="255ca-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="255ca-130">-FirstName</span></span>
<span data-ttu-id="255ca-131">Kullanıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="255ca-131">Specifies the first name of the user.</span></span>
<span data-ttu-id="255ca-132">Bu parametre belirtilmişse, bu cmdlet bir kullanıcıyı adıyla bulur.</span><span class="sxs-lookup"><span data-stu-id="255ca-132">If this parameter is specified, this cmdlet finds a user by first name.</span></span>
<span data-ttu-id="255ca-133">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="255ca-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="255ca-134">-GroupID</span><span class="sxs-lookup"><span data-stu-id="255ca-134">-GroupId</span></span>
<span data-ttu-id="255ca-135">Grup tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="255ca-135">Specifies the group identifier.</span></span>
<span data-ttu-id="255ca-136">Belirtilmişse, bu cmdlet belirtilen gruptaki tüm kullanıcıları bulur.</span><span class="sxs-lookup"><span data-stu-id="255ca-136">If specified, this cmdlet finds all users within the specified group.</span></span>
<span data-ttu-id="255ca-137">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="255ca-137">This parameter is optional.</span></span>

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

### <span data-ttu-id="255ca-138">-LastName</span><span class="sxs-lookup"><span data-stu-id="255ca-138">-LastName</span></span>
<span data-ttu-id="255ca-139">Kullanıcının soyadını belirtir.</span><span class="sxs-lookup"><span data-stu-id="255ca-139">Specifies the last name of a user.</span></span>
<span data-ttu-id="255ca-140">Belirtilmişse, bu cmdlet kullanıcıları soyadına göre bulur.</span><span class="sxs-lookup"><span data-stu-id="255ca-140">If specified, this cmdlet finds users by last name.</span></span>
<span data-ttu-id="255ca-141">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="255ca-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="255ca-142">Durumlu</span><span class="sxs-lookup"><span data-stu-id="255ca-142">-State</span></span>
<span data-ttu-id="255ca-143">Kullanıcı durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="255ca-143">Specifies the user state.</span></span>
<span data-ttu-id="255ca-144">Belirtilmişse bu cmdlet bu durumda kullanıcıları bulur.</span><span class="sxs-lookup"><span data-stu-id="255ca-144">If specified, this cmdlet finds users in this state.</span></span>
<span data-ttu-id="255ca-145">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="255ca-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="255ca-146">-UserID</span><span class="sxs-lookup"><span data-stu-id="255ca-146">-UserId</span></span>
<span data-ttu-id="255ca-147">Bir kullanıcı KIMLIĞI belirtir.</span><span class="sxs-lookup"><span data-stu-id="255ca-147">Specifies a user ID.</span></span>
<span data-ttu-id="255ca-148">Belirtilmişse, bu cmdlet kullanıcıyı bu tanımlayıcıyla bulur.</span><span class="sxs-lookup"><span data-stu-id="255ca-148">If specified, this cmdlet finds the user by this identifier.</span></span>
<span data-ttu-id="255ca-149">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="255ca-149">This parameter is optional.</span></span>

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

### <span data-ttu-id="255ca-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="255ca-150">CommonParameters</span></span>
<span data-ttu-id="255ca-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="255ca-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="255ca-152">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="255ca-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="255ca-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="255ca-153">INPUTS</span></span>

### <span data-ttu-id="255ca-154">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="255ca-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="255ca-155">System. String</span><span class="sxs-lookup"><span data-stu-id="255ca-155">System.String</span></span>

### <span data-ttu-id="255ca-156">System. Nullable ' 1 [[Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementuserstate, Microsoft. Azure. PowerShell. cmdlet</span><span class="sxs-lookup"><span data-stu-id="255ca-156">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="255ca-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="255ca-157">OUTPUTS</span></span>

### <span data-ttu-id="255ca-158">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementuser</span><span class="sxs-lookup"><span data-stu-id="255ca-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="255ca-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="255ca-159">NOTES</span></span>

## <span data-ttu-id="255ca-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="255ca-160">RELATED LINKS</span></span>

[<span data-ttu-id="255ca-161">Yeni-Azsız Kullanıcı</span><span class="sxs-lookup"><span data-stu-id="255ca-161">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="255ca-162">Remove-Azapsananagementuser</span><span class="sxs-lookup"><span data-stu-id="255ca-162">Remove-AzApiManagementUser</span></span>](./Remove-AzApiManagementUser.md)

[<span data-ttu-id="255ca-163">Set-Azapsananagementuser</span><span class="sxs-lookup"><span data-stu-id="255ca-163">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


