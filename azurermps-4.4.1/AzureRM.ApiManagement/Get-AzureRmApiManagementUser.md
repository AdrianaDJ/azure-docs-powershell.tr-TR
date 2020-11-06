---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 638B2BF6-23F8-4038-B20B-1CFABFDBF5D3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
ms.openlocfilehash: be6c9ee6c0db12e324786052348209703b79601e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587040"
---
# <span data-ttu-id="e932e-101">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="e932e-101">Get-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="e932e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e932e-102">SYNOPSIS</span></span>
<span data-ttu-id="e932e-103">Bir kullanıcıyı veya kullanıcıları alır.</span><span class="sxs-lookup"><span data-stu-id="e932e-103">Gets a user or users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e932e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e932e-104">SYNTAX</span></span>

### <span data-ttu-id="e932e-105">Tüm kullanıcıları al (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e932e-105">Get all users (Default)</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e932e-106">KIMLIĞE göre Kullanıcı alma</span><span class="sxs-lookup"><span data-stu-id="e932e-106">Get user by ID</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e932e-107">Kullanıcıları bulma</span><span class="sxs-lookup"><span data-stu-id="e932e-107">Find users</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-FirstName <String>] [-LastName <String>]
 [-State <PsApiManagementUserState>] [-Email <String>] [-GroupId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e932e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e932e-108">DESCRIPTION</span></span>
<span data-ttu-id="e932e-109">**Get-Azurermapsananagementuser** cmdlet 'i belirtilen kullanıcıyı veya herhangi bir Kullanıcı belirtilmemişse tüm kullanıcıları alır.</span><span class="sxs-lookup"><span data-stu-id="e932e-109">The **Get-AzureRmApiManagementUser** cmdlet gets a specified user, or all users, if no user is specified.</span></span>

## <span data-ttu-id="e932e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e932e-110">EXAMPLES</span></span>

### <span data-ttu-id="e932e-111">Örnek 1: tüm kullanıcıları alma</span><span class="sxs-lookup"><span data-stu-id="e932e-111">Example 1: Get all users</span></span>
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext
```

<span data-ttu-id="e932e-112">Bu komut tüm kullanıcıları alır.</span><span class="sxs-lookup"><span data-stu-id="e932e-112">This command gets all users.</span></span>

### <span data-ttu-id="e932e-113">Örnek 2: KIMLIĞE göre bir Kullanıcı alma</span><span class="sxs-lookup"><span data-stu-id="e932e-113">Example 2: Get a user by ID</span></span>
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="e932e-114">Bu komut bir kullanıcıyı KIMLIĞE göre alır.</span><span class="sxs-lookup"><span data-stu-id="e932e-114">This command gets a user by ID.</span></span>

### <span data-ttu-id="e932e-115">Örnek: kullanıcıları soyadına göre alma</span><span class="sxs-lookup"><span data-stu-id="e932e-115">Example: Get users by last name</span></span>
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -LastName "Fuller"
```

<span data-ttu-id="e932e-116">Bu komut, belirli bir soyadınız olan kullanıcıları alır.</span><span class="sxs-lookup"><span data-stu-id="e932e-116">This command gets users that have a specified last name, Fuller.</span></span>

### <span data-ttu-id="e932e-117">Örnek 4: e-posta adresine göre Kullanıcı alma</span><span class="sxs-lookup"><span data-stu-id="e932e-117">Example 4: Get a user by email address</span></span>
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -Email 
"user@contoso.com"
```

<span data-ttu-id="e932e-118">Bu komut, belirtilen e-posta adresine sahip kullanıcıyı alır.</span><span class="sxs-lookup"><span data-stu-id="e932e-118">This command gets the user that has the specified email address.</span></span>

### <span data-ttu-id="e932e-119">Örnek 5: Grup içindeki tüm kullanıcıları alma</span><span class="sxs-lookup"><span data-stu-id="e932e-119">Example 5: Get all users within a group</span></span>
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -GroupId "0001"
```

<span data-ttu-id="e932e-120">Bu komut belirtilen gruptaki tüm kullanıcıları alır.</span><span class="sxs-lookup"><span data-stu-id="e932e-120">This command gets all users within the specified group.</span></span>

## <span data-ttu-id="e932e-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e932e-121">PARAMETERS</span></span>

### <span data-ttu-id="e932e-122">-Context</span><span class="sxs-lookup"><span data-stu-id="e932e-122">-Context</span></span>
<span data-ttu-id="e932e-123">**Psapsananagementcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e932e-123">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="e932e-124">-E-posta</span><span class="sxs-lookup"><span data-stu-id="e932e-124">-Email</span></span>
<span data-ttu-id="e932e-125">Kullanıcının e-posta adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e932e-125">Specifies the email address of the user.</span></span>
<span data-ttu-id="e932e-126">Bu parametre belirtilmişse, bu cmdlet bir kullanıcıyı e-posta ile bulur.</span><span class="sxs-lookup"><span data-stu-id="e932e-126">If this parameter is specified, this cmdlet finds a user by email.</span></span>
<span data-ttu-id="e932e-127">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="e932e-127">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e932e-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="e932e-128">-FirstName</span></span>
<span data-ttu-id="e932e-129">Kullanıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e932e-129">Specifies the first name of the user.</span></span>
<span data-ttu-id="e932e-130">Bu parametre belirtilmişse, bu cmdlet bir kullanıcıyı adıyla bulur.</span><span class="sxs-lookup"><span data-stu-id="e932e-130">If this parameter is specified, this cmdlet finds a user by first name.</span></span>
<span data-ttu-id="e932e-131">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="e932e-131">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e932e-132">-GroupID</span><span class="sxs-lookup"><span data-stu-id="e932e-132">-GroupId</span></span>
<span data-ttu-id="e932e-133">Grup tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e932e-133">Specifies the group identifier.</span></span>
<span data-ttu-id="e932e-134">Belirtilmişse, bu cmdlet belirtilen gruptaki tüm kullanıcıları bulur.</span><span class="sxs-lookup"><span data-stu-id="e932e-134">If specified, this cmdlet finds all users within the specified group.</span></span>
<span data-ttu-id="e932e-135">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="e932e-135">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e932e-136">-LastName</span><span class="sxs-lookup"><span data-stu-id="e932e-136">-LastName</span></span>
<span data-ttu-id="e932e-137">Kullanıcının soyadını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e932e-137">Specifies the last name of a user.</span></span>
<span data-ttu-id="e932e-138">Belirtilmişse, bu cmdlet kullanıcıları soyadına göre bulur.</span><span class="sxs-lookup"><span data-stu-id="e932e-138">If specified, this cmdlet finds users by last name.</span></span>
<span data-ttu-id="e932e-139">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="e932e-139">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e932e-140">Durumlu</span><span class="sxs-lookup"><span data-stu-id="e932e-140">-State</span></span>
<span data-ttu-id="e932e-141">Kullanıcı durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e932e-141">Specifies the user state.</span></span>
<span data-ttu-id="e932e-142">Belirtilmişse bu cmdlet bu durumda kullanıcıları bulur.</span><span class="sxs-lookup"><span data-stu-id="e932e-142">If specified, this cmdlet finds users in this state.</span></span>
<span data-ttu-id="e932e-143">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="e932e-143">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: Find users
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e932e-144">-UserID</span><span class="sxs-lookup"><span data-stu-id="e932e-144">-UserId</span></span>
<span data-ttu-id="e932e-145">Bir kullanıcı KIMLIĞI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e932e-145">Specifies a user ID.</span></span>
<span data-ttu-id="e932e-146">Belirtilmişse, bu cmdlet kullanıcıyı bu tanımlayıcıyla bulur.</span><span class="sxs-lookup"><span data-stu-id="e932e-146">If specified, this cmdlet finds the user by this identifier.</span></span>
<span data-ttu-id="e932e-147">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="e932e-147">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Get user by ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e932e-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e932e-148">-DefaultProfile</span></span>
<span data-ttu-id="e932e-149">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e932e-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e932e-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e932e-150">CommonParameters</span></span>
<span data-ttu-id="e932e-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e932e-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e932e-152">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e932e-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e932e-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e932e-153">INPUTS</span></span>

## <span data-ttu-id="e932e-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e932e-154">OUTPUTS</span></span>

### <span data-ttu-id="e932e-155">IList<Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementuser></span><span class="sxs-lookup"><span data-stu-id="e932e-155">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser></span></span>

## <span data-ttu-id="e932e-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e932e-156">NOTES</span></span>

## <span data-ttu-id="e932e-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e932e-157">RELATED LINKS</span></span>

[<span data-ttu-id="e932e-158">Yeni-Azurermapımanagementuser</span><span class="sxs-lookup"><span data-stu-id="e932e-158">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="e932e-159">Remove-Azurermapsananagementuser</span><span class="sxs-lookup"><span data-stu-id="e932e-159">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)

[<span data-ttu-id="e932e-160">Set-Azurermapımanagementuser</span><span class="sxs-lookup"><span data-stu-id="e932e-160">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


