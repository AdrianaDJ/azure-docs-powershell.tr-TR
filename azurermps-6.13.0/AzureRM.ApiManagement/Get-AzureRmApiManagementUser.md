---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 638B2BF6-23F8-4038-B20B-1CFABFDBF5D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
ms.openlocfilehash: 8f02b88115ec6dc415ecf6cf5464503d61778cca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591472"
---
# <span data-ttu-id="51d77-101">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="51d77-101">Get-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="51d77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51d77-102">SYNOPSIS</span></span>
<span data-ttu-id="51d77-103">Bir kullanıcıyı veya kullanıcıları alır.</span><span class="sxs-lookup"><span data-stu-id="51d77-103">Gets a user or users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51d77-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="51d77-104">SYNTAX</span></span>

### <span data-ttu-id="51d77-105">GeAllUsers (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="51d77-105">GeAllUsers (Default)</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="51d77-106">Getbyuserıd</span><span class="sxs-lookup"><span data-stu-id="51d77-106">GetByUserId</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51d77-107">GetByUser</span><span class="sxs-lookup"><span data-stu-id="51d77-107">GetByUser</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-FirstName <String>] [-LastName <String>]
 [-State <PsApiManagementUserState>] [-Email <String>] [-GroupId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51d77-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="51d77-108">DESCRIPTION</span></span>
<span data-ttu-id="51d77-109">**Get-Azurermapsananagementuser** cmdlet 'i belirtilen kullanıcıyı veya herhangi bir Kullanıcı belirtilmemişse tüm kullanıcıları alır.</span><span class="sxs-lookup"><span data-stu-id="51d77-109">The **Get-AzureRmApiManagementUser** cmdlet gets a specified user, or all users, if no user is specified.</span></span>

## <span data-ttu-id="51d77-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="51d77-110">EXAMPLES</span></span>

### <span data-ttu-id="51d77-111">Örnek 1: tüm kullanıcıları alma</span><span class="sxs-lookup"><span data-stu-id="51d77-111">Example 1: Get all users</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext
```

<span data-ttu-id="51d77-112">Bu komut tüm kullanıcıları alır.</span><span class="sxs-lookup"><span data-stu-id="51d77-112">This command gets all users.</span></span>

### <span data-ttu-id="51d77-113">Örnek 2: KIMLIĞE göre bir Kullanıcı alma</span><span class="sxs-lookup"><span data-stu-id="51d77-113">Example 2: Get a user by ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="51d77-114">Bu komut bir kullanıcıyı KIMLIĞE göre alır.</span><span class="sxs-lookup"><span data-stu-id="51d77-114">This command gets a user by ID.</span></span>

### <span data-ttu-id="51d77-115">Örnek: kullanıcıları soyadına göre alma</span><span class="sxs-lookup"><span data-stu-id="51d77-115">Example: Get users by last name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -LastName "Fuller"
```

<span data-ttu-id="51d77-116">Bu komut, belirli bir soyadınız olan kullanıcıları alır.</span><span class="sxs-lookup"><span data-stu-id="51d77-116">This command gets users that have a specified last name, Fuller.</span></span>

### <span data-ttu-id="51d77-117">Örnek 4: e-posta adresine göre Kullanıcı alma</span><span class="sxs-lookup"><span data-stu-id="51d77-117">Example 4: Get a user by email address</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -Email "user@contoso.com"
```

<span data-ttu-id="51d77-118">Bu komut, belirtilen e-posta adresine sahip kullanıcıyı alır.</span><span class="sxs-lookup"><span data-stu-id="51d77-118">This command gets the user that has the specified email address.</span></span>

### <span data-ttu-id="51d77-119">Örnek 5: Grup içindeki tüm kullanıcıları alma</span><span class="sxs-lookup"><span data-stu-id="51d77-119">Example 5: Get all users within a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -GroupId "0001"
```

<span data-ttu-id="51d77-120">Bu komut belirtilen gruptaki tüm kullanıcıları alır.</span><span class="sxs-lookup"><span data-stu-id="51d77-120">This command gets all users within the specified group.</span></span>

## <span data-ttu-id="51d77-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="51d77-121">PARAMETERS</span></span>

### <span data-ttu-id="51d77-122">-Context</span><span class="sxs-lookup"><span data-stu-id="51d77-122">-Context</span></span>
<span data-ttu-id="51d77-123">**Psapsananagementcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="51d77-123">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="51d77-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51d77-124">-DefaultProfile</span></span>
<span data-ttu-id="51d77-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="51d77-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51d77-126">-E-posta</span><span class="sxs-lookup"><span data-stu-id="51d77-126">-Email</span></span>
<span data-ttu-id="51d77-127">Kullanıcının e-posta adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="51d77-127">Specifies the email address of the user.</span></span>
<span data-ttu-id="51d77-128">Bu parametre belirtilmişse, bu cmdlet bir kullanıcıyı e-posta ile bulur.</span><span class="sxs-lookup"><span data-stu-id="51d77-128">If this parameter is specified, this cmdlet finds a user by email.</span></span>
<span data-ttu-id="51d77-129">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="51d77-129">This parameter is optional.</span></span>

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

### <span data-ttu-id="51d77-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="51d77-130">-FirstName</span></span>
<span data-ttu-id="51d77-131">Kullanıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="51d77-131">Specifies the first name of the user.</span></span>
<span data-ttu-id="51d77-132">Bu parametre belirtilmişse, bu cmdlet bir kullanıcıyı adıyla bulur.</span><span class="sxs-lookup"><span data-stu-id="51d77-132">If this parameter is specified, this cmdlet finds a user by first name.</span></span>
<span data-ttu-id="51d77-133">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="51d77-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="51d77-134">-GroupID</span><span class="sxs-lookup"><span data-stu-id="51d77-134">-GroupId</span></span>
<span data-ttu-id="51d77-135">Grup tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="51d77-135">Specifies the group identifier.</span></span>
<span data-ttu-id="51d77-136">Belirtilmişse, bu cmdlet belirtilen gruptaki tüm kullanıcıları bulur.</span><span class="sxs-lookup"><span data-stu-id="51d77-136">If specified, this cmdlet finds all users within the specified group.</span></span>
<span data-ttu-id="51d77-137">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="51d77-137">This parameter is optional.</span></span>

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

### <span data-ttu-id="51d77-138">-LastName</span><span class="sxs-lookup"><span data-stu-id="51d77-138">-LastName</span></span>
<span data-ttu-id="51d77-139">Kullanıcının soyadını belirtir.</span><span class="sxs-lookup"><span data-stu-id="51d77-139">Specifies the last name of a user.</span></span>
<span data-ttu-id="51d77-140">Belirtilmişse, bu cmdlet kullanıcıları soyadına göre bulur.</span><span class="sxs-lookup"><span data-stu-id="51d77-140">If specified, this cmdlet finds users by last name.</span></span>
<span data-ttu-id="51d77-141">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="51d77-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="51d77-142">Durumlu</span><span class="sxs-lookup"><span data-stu-id="51d77-142">-State</span></span>
<span data-ttu-id="51d77-143">Kullanıcı durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="51d77-143">Specifies the user state.</span></span>
<span data-ttu-id="51d77-144">Belirtilmişse bu cmdlet bu durumda kullanıcıları bulur.</span><span class="sxs-lookup"><span data-stu-id="51d77-144">If specified, this cmdlet finds users in this state.</span></span>
<span data-ttu-id="51d77-145">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="51d77-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="51d77-146">-UserID</span><span class="sxs-lookup"><span data-stu-id="51d77-146">-UserId</span></span>
<span data-ttu-id="51d77-147">Bir kullanıcı KIMLIĞI belirtir.</span><span class="sxs-lookup"><span data-stu-id="51d77-147">Specifies a user ID.</span></span>
<span data-ttu-id="51d77-148">Belirtilmişse, bu cmdlet kullanıcıyı bu tanımlayıcıyla bulur.</span><span class="sxs-lookup"><span data-stu-id="51d77-148">If specified, this cmdlet finds the user by this identifier.</span></span>
<span data-ttu-id="51d77-149">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="51d77-149">This parameter is optional.</span></span>

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

### <span data-ttu-id="51d77-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51d77-150">CommonParameters</span></span>
<span data-ttu-id="51d77-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="51d77-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51d77-152">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51d77-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51d77-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="51d77-153">INPUTS</span></span>

### <span data-ttu-id="51d77-154">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="51d77-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="51d77-155">System. String</span><span class="sxs-lookup"><span data-stu-id="51d77-155">System.String</span></span>

### <span data-ttu-id="51d77-156">System. Nullable ' 1 [[Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementuserstate, Microsoft. Azure. Commands</span><span class="sxs-lookup"><span data-stu-id="51d77-156">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.Commands.ApiManagement.ServiceManagement, Version=6.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="51d77-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="51d77-157">OUTPUTS</span></span>

### <span data-ttu-id="51d77-158">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementuser</span><span class="sxs-lookup"><span data-stu-id="51d77-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="51d77-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="51d77-159">NOTES</span></span>

## <span data-ttu-id="51d77-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="51d77-160">RELATED LINKS</span></span>

[<span data-ttu-id="51d77-161">Yeni-Azurermapımanagementuser</span><span class="sxs-lookup"><span data-stu-id="51d77-161">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="51d77-162">Remove-Azurermapsananagementuser</span><span class="sxs-lookup"><span data-stu-id="51d77-162">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)

[<span data-ttu-id="51d77-163">Set-Azurermapımanagementuser</span><span class="sxs-lookup"><span data-stu-id="51d77-163">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


