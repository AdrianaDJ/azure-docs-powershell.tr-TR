---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
ms.openlocfilehash: 6cc922ceb09509e70a4017241dc6beb6e5443d1a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097685"
---
# <span data-ttu-id="65942-101">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="65942-101">New-AzApiManagementUser</span></span>

## <span data-ttu-id="65942-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65942-102">SYNOPSIS</span></span>
<span data-ttu-id="65942-103">Yeni bir kullanıcı kaydeder.</span><span class="sxs-lookup"><span data-stu-id="65942-103">Registers a new user.</span></span>

## <span data-ttu-id="65942-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="65942-104">SYNTAX</span></span>

```
New-AzApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <SecureString> [-State <PsApiManagementUserState>]
 [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65942-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="65942-105">DESCRIPTION</span></span>
<span data-ttu-id="65942-106">**Yeni-Azsız Kullanıcı** cmdlet 'i yeni bir kullanıcı kaydeder.</span><span class="sxs-lookup"><span data-stu-id="65942-106">The **New-AzApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="65942-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="65942-107">EXAMPLES</span></span>

### <span data-ttu-id="65942-108">Örnek 1: yeni bir kullanıcıyı kaydettirme</span><span class="sxs-lookup"><span data-stu-id="65942-108">Example 1: Register a new user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>New-AzApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password $securePassword
```

<span data-ttu-id="65942-109">Bu komut, Patti Fuller adlı yeni bir kullanıcı kaydeder.</span><span class="sxs-lookup"><span data-stu-id="65942-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="65942-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="65942-110">PARAMETERS</span></span>

### <span data-ttu-id="65942-111">-Context</span><span class="sxs-lookup"><span data-stu-id="65942-111">-Context</span></span>
<span data-ttu-id="65942-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="65942-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="65942-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65942-113">-DefaultProfile</span></span>
<span data-ttu-id="65942-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="65942-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65942-115">-E-posta</span><span class="sxs-lookup"><span data-stu-id="65942-115">-Email</span></span>
<span data-ttu-id="65942-116">Kullanıcının e-posta adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="65942-116">Specifies the email address of the user.</span></span>

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

### <span data-ttu-id="65942-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="65942-117">-FirstName</span></span>
<span data-ttu-id="65942-118">Kullanıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="65942-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="65942-119">Bu parametre 1-100 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="65942-119">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="65942-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="65942-120">-LastName</span></span>
<span data-ttu-id="65942-121">Kullanıcının soyadını belirtir.</span><span class="sxs-lookup"><span data-stu-id="65942-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="65942-122">Bu parametre 1-100 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="65942-122">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="65942-123">Not</span><span class="sxs-lookup"><span data-stu-id="65942-123">-Note</span></span>
<span data-ttu-id="65942-124">Kullanıcı hakkında bir Not belirtir.</span><span class="sxs-lookup"><span data-stu-id="65942-124">Specifies a note about the user.</span></span>
<span data-ttu-id="65942-125">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="65942-125">This parameter is optional.</span></span>
<span data-ttu-id="65942-126">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="65942-126">The default value is $Null.</span></span>

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

### <span data-ttu-id="65942-127">-Parola</span><span class="sxs-lookup"><span data-stu-id="65942-127">-Password</span></span>
<span data-ttu-id="65942-128">Kullanıcı parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="65942-128">Specifies the user password.</span></span>
<span data-ttu-id="65942-129">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="65942-129">This parameter is required.</span></span>

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

### <span data-ttu-id="65942-130">Durumlu</span><span class="sxs-lookup"><span data-stu-id="65942-130">-State</span></span>
<span data-ttu-id="65942-131">Kullanıcı durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="65942-131">Specifies the user state.</span></span>
<span data-ttu-id="65942-132">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="65942-132">This parameter is optional.</span></span>
<span data-ttu-id="65942-133">Bu parametrenin varsayılan değeri $Null.</span><span class="sxs-lookup"><span data-stu-id="65942-133">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: (All)
Aliases:
Accepted values: Active, Blocked, Deleted, Pending

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65942-134">-UserID</span><span class="sxs-lookup"><span data-stu-id="65942-134">-UserId</span></span>
<span data-ttu-id="65942-135">Kullanıcı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="65942-135">Specifies the user ID.</span></span>
<span data-ttu-id="65942-136">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="65942-136">This parameter is optional.</span></span>
<span data-ttu-id="65942-137">Bu parametre belirtilmezse, bu cmdlet bir kullanıcı KIMLIĞI oluşturur.</span><span class="sxs-lookup"><span data-stu-id="65942-137">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

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

### <span data-ttu-id="65942-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65942-138">CommonParameters</span></span>
<span data-ttu-id="65942-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="65942-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65942-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="65942-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65942-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="65942-141">INPUTS</span></span>

### <span data-ttu-id="65942-142">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="65942-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="65942-143">System. String</span><span class="sxs-lookup"><span data-stu-id="65942-143">System.String</span></span>

### <span data-ttu-id="65942-144">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="65942-144">System.Security.SecureString</span></span>

### <span data-ttu-id="65942-145">System. Nullable ' 1 [[Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementuserstate, Microsoft. Azure. PowerShell. cmdlet</span><span class="sxs-lookup"><span data-stu-id="65942-145">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="65942-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="65942-146">OUTPUTS</span></span>

### <span data-ttu-id="65942-147">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementuser</span><span class="sxs-lookup"><span data-stu-id="65942-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="65942-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="65942-148">NOTES</span></span>

## <span data-ttu-id="65942-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="65942-149">RELATED LINKS</span></span>

[<span data-ttu-id="65942-150">Get-Azsız Kullanıcı</span><span class="sxs-lookup"><span data-stu-id="65942-150">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="65942-151">Set-Azapsananagementuser</span><span class="sxs-lookup"><span data-stu-id="65942-151">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


