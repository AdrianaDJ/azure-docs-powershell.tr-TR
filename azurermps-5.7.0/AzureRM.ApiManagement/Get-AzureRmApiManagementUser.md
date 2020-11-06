---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 638B2BF6-23F8-4038-B20B-1CFABFDBF5D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
ms.openlocfilehash: 07f387239bdaad526c36c3928e7d2c5f490b0c7b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589915"
---
# <span data-ttu-id="62b31-101">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="62b31-101">Get-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="62b31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62b31-102">SYNOPSIS</span></span>
<span data-ttu-id="62b31-103">Bir kullanıcıyı veya kullanıcıları alır.</span><span class="sxs-lookup"><span data-stu-id="62b31-103">Gets a user or users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62b31-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="62b31-104">SYNTAX</span></span>

### <span data-ttu-id="62b31-105">GeAllUsers (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="62b31-105">GeAllUsers (Default)</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="62b31-106">Getbyuserıd</span><span class="sxs-lookup"><span data-stu-id="62b31-106">GetByUserId</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62b31-107">GetByUser</span><span class="sxs-lookup"><span data-stu-id="62b31-107">GetByUser</span></span>
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-FirstName <String>] [-LastName <String>]
 [-State <PsApiManagementUserState>] [-Email <String>] [-GroupId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62b31-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="62b31-108">DESCRIPTION</span></span>
<span data-ttu-id="62b31-109">**Get-Azurermapsananagementuser** cmdlet 'i belirtilen kullanıcıyı veya herhangi bir Kullanıcı belirtilmemişse tüm kullanıcıları alır.</span><span class="sxs-lookup"><span data-stu-id="62b31-109">The **Get-AzureRmApiManagementUser** cmdlet gets a specified user, or all users, if no user is specified.</span></span>

## <span data-ttu-id="62b31-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="62b31-110">EXAMPLES</span></span>

### <span data-ttu-id="62b31-111">Örnek 1: tüm kullanıcıları alma</span><span class="sxs-lookup"><span data-stu-id="62b31-111">Example 1: Get all users</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext
```

<span data-ttu-id="62b31-112">Bu komut tüm kullanıcıları alır.</span><span class="sxs-lookup"><span data-stu-id="62b31-112">This command gets all users.</span></span>

### <span data-ttu-id="62b31-113">Örnek 2: KIMLIĞE göre bir Kullanıcı alma</span><span class="sxs-lookup"><span data-stu-id="62b31-113">Example 2: Get a user by ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="62b31-114">Bu komut bir kullanıcıyı KIMLIĞE göre alır.</span><span class="sxs-lookup"><span data-stu-id="62b31-114">This command gets a user by ID.</span></span>

### <span data-ttu-id="62b31-115">Örnek: kullanıcıları soyadına göre alma</span><span class="sxs-lookup"><span data-stu-id="62b31-115">Example: Get users by last name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -LastName "Fuller"
```

<span data-ttu-id="62b31-116">Bu komut, belirli bir soyadınız olan kullanıcıları alır.</span><span class="sxs-lookup"><span data-stu-id="62b31-116">This command gets users that have a specified last name, Fuller.</span></span>

### <span data-ttu-id="62b31-117">Örnek 4: e-posta adresine göre Kullanıcı alma</span><span class="sxs-lookup"><span data-stu-id="62b31-117">Example 4: Get a user by email address</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -Email "user@contoso.com"
```

<span data-ttu-id="62b31-118">Bu komut, belirtilen e-posta adresine sahip kullanıcıyı alır.</span><span class="sxs-lookup"><span data-stu-id="62b31-118">This command gets the user that has the specified email address.</span></span>

### <span data-ttu-id="62b31-119">Örnek 5: Grup içindeki tüm kullanıcıları alma</span><span class="sxs-lookup"><span data-stu-id="62b31-119">Example 5: Get all users within a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -GroupId "0001"
```

<span data-ttu-id="62b31-120">Bu komut belirtilen gruptaki tüm kullanıcıları alır.</span><span class="sxs-lookup"><span data-stu-id="62b31-120">This command gets all users within the specified group.</span></span>

## <span data-ttu-id="62b31-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="62b31-121">PARAMETERS</span></span>

### <span data-ttu-id="62b31-122">-Context</span><span class="sxs-lookup"><span data-stu-id="62b31-122">-Context</span></span>
<span data-ttu-id="62b31-123">**Psapsananagementcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="62b31-123">Specifies an instance of **PsApiManagementContext**.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62b31-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62b31-124">-DefaultProfile</span></span>
<span data-ttu-id="62b31-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="62b31-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62b31-126">-E-posta</span><span class="sxs-lookup"><span data-stu-id="62b31-126">-Email</span></span>
<span data-ttu-id="62b31-127">Kullanıcının e-posta adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="62b31-127">Specifies the email address of the user.</span></span>
<span data-ttu-id="62b31-128">Bu parametre belirtilmişse, bu cmdlet bir kullanıcıyı e-posta ile bulur.</span><span class="sxs-lookup"><span data-stu-id="62b31-128">If this parameter is specified, this cmdlet finds a user by email.</span></span>
<span data-ttu-id="62b31-129">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="62b31-129">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByUser
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62b31-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="62b31-130">-FirstName</span></span>
<span data-ttu-id="62b31-131">Kullanıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="62b31-131">Specifies the first name of the user.</span></span>
<span data-ttu-id="62b31-132">Bu parametre belirtilmişse, bu cmdlet bir kullanıcıyı adıyla bulur.</span><span class="sxs-lookup"><span data-stu-id="62b31-132">If this parameter is specified, this cmdlet finds a user by first name.</span></span>
<span data-ttu-id="62b31-133">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="62b31-133">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByUser
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62b31-134">-GroupID</span><span class="sxs-lookup"><span data-stu-id="62b31-134">-GroupId</span></span>
<span data-ttu-id="62b31-135">Grup tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="62b31-135">Specifies the group identifier.</span></span>
<span data-ttu-id="62b31-136">Belirtilmişse, bu cmdlet belirtilen gruptaki tüm kullanıcıları bulur.</span><span class="sxs-lookup"><span data-stu-id="62b31-136">If specified, this cmdlet finds all users within the specified group.</span></span>
<span data-ttu-id="62b31-137">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="62b31-137">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByUser
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62b31-138">-LastName</span><span class="sxs-lookup"><span data-stu-id="62b31-138">-LastName</span></span>
<span data-ttu-id="62b31-139">Kullanıcının soyadını belirtir.</span><span class="sxs-lookup"><span data-stu-id="62b31-139">Specifies the last name of a user.</span></span>
<span data-ttu-id="62b31-140">Belirtilmişse, bu cmdlet kullanıcıları soyadına göre bulur.</span><span class="sxs-lookup"><span data-stu-id="62b31-140">If specified, this cmdlet finds users by last name.</span></span>
<span data-ttu-id="62b31-141">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="62b31-141">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByUser
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62b31-142">Durumlu</span><span class="sxs-lookup"><span data-stu-id="62b31-142">-State</span></span>
<span data-ttu-id="62b31-143">Kullanıcı durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="62b31-143">Specifies the user state.</span></span>
<span data-ttu-id="62b31-144">Belirtilmişse bu cmdlet bu durumda kullanıcıları bulur.</span><span class="sxs-lookup"><span data-stu-id="62b31-144">If specified, this cmdlet finds users in this state.</span></span>
<span data-ttu-id="62b31-145">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="62b31-145">This parameter is optional.</span></span>

```yaml
Type: PsApiManagementUserState
Parameter Sets: GetByUser
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62b31-146">-UserID</span><span class="sxs-lookup"><span data-stu-id="62b31-146">-UserId</span></span>
<span data-ttu-id="62b31-147">Bir kullanıcı KIMLIĞI belirtir.</span><span class="sxs-lookup"><span data-stu-id="62b31-147">Specifies a user ID.</span></span>
<span data-ttu-id="62b31-148">Belirtilmişse, bu cmdlet kullanıcıyı bu tanımlayıcıyla bulur.</span><span class="sxs-lookup"><span data-stu-id="62b31-148">If specified, this cmdlet finds the user by this identifier.</span></span>
<span data-ttu-id="62b31-149">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="62b31-149">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByUserId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62b31-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62b31-150">CommonParameters</span></span>
<span data-ttu-id="62b31-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="62b31-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62b31-152">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62b31-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62b31-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="62b31-153">INPUTS</span></span>

### <span data-ttu-id="62b31-154">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="62b31-154">None</span></span>
<span data-ttu-id="62b31-155">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="62b31-155">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="62b31-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="62b31-156">OUTPUTS</span></span>

### <span data-ttu-id="62b31-157">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementuser</span><span class="sxs-lookup"><span data-stu-id="62b31-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>
<span data-ttu-id="62b31-158">API yönetim hizmetindeki kullanıcının ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="62b31-158">The details of User in API Management service.</span></span>

### <span data-ttu-id="62b31-159">IList<Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementuser></span><span class="sxs-lookup"><span data-stu-id="62b31-159">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser></span></span>
<span data-ttu-id="62b31-160">API yönetim hizmetindeki Kullanıcı listesi.</span><span class="sxs-lookup"><span data-stu-id="62b31-160">The list of User in the API Management  service.</span></span>

## <span data-ttu-id="62b31-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="62b31-161">NOTES</span></span>

## <span data-ttu-id="62b31-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="62b31-162">RELATED LINKS</span></span>

[<span data-ttu-id="62b31-163">Yeni-Azurermapımanagementuser</span><span class="sxs-lookup"><span data-stu-id="62b31-163">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="62b31-164">Remove-Azurermapsananagementuser</span><span class="sxs-lookup"><span data-stu-id="62b31-164">Remove-AzureRmApiManagementUser</span></span>](./Remove-AzureRmApiManagementUser.md)

[<span data-ttu-id="62b31-165">Set-Azurermapımanagementuser</span><span class="sxs-lookup"><span data-stu-id="62b31-165">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


