---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUser.md
ms.openlocfilehash: d8d88c2071cafad33fd4a80cb4c2de63ccf89647
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753497"
---
# <span data-ttu-id="1fca7-101">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="1fca7-101">New-AzApiManagementUser</span></span>

## <span data-ttu-id="1fca7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fca7-102">SYNOPSIS</span></span>
<span data-ttu-id="1fca7-103">Yeni bir kullanıcı kaydeder.</span><span class="sxs-lookup"><span data-stu-id="1fca7-103">Registers a new user.</span></span>

## <span data-ttu-id="1fca7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1fca7-104">SYNTAX</span></span>

```
New-AzApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <SecureString> [-State <PsApiManagementUserState>]
 [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1fca7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1fca7-105">DESCRIPTION</span></span>
<span data-ttu-id="1fca7-106">**Yeni-Azsız Kullanıcı** cmdlet 'i yeni bir kullanıcı kaydeder.</span><span class="sxs-lookup"><span data-stu-id="1fca7-106">The **New-AzApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="1fca7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1fca7-107">EXAMPLES</span></span>

### <span data-ttu-id="1fca7-108">Örnek 1: yeni bir kullanıcıyı kaydettirme</span><span class="sxs-lookup"><span data-stu-id="1fca7-108">Example 1: Register a new user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>New-AzApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password $securePassword
```

<span data-ttu-id="1fca7-109">Bu komut, Patti Fuller adlı yeni bir kullanıcı kaydeder.</span><span class="sxs-lookup"><span data-stu-id="1fca7-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="1fca7-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1fca7-110">PARAMETERS</span></span>

### <span data-ttu-id="1fca7-111">-Context</span><span class="sxs-lookup"><span data-stu-id="1fca7-111">-Context</span></span>
<span data-ttu-id="1fca7-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1fca7-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1fca7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fca7-113">-DefaultProfile</span></span>
<span data-ttu-id="1fca7-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1fca7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1fca7-115">-E-posta</span><span class="sxs-lookup"><span data-stu-id="1fca7-115">-Email</span></span>
<span data-ttu-id="1fca7-116">Kullanıcının e-posta adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1fca7-116">Specifies the email address of the user.</span></span>

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

### <span data-ttu-id="1fca7-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="1fca7-117">-FirstName</span></span>
<span data-ttu-id="1fca7-118">Kullanıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1fca7-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="1fca7-119">Bu parametre 1-100 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="1fca7-119">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="1fca7-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="1fca7-120">-LastName</span></span>
<span data-ttu-id="1fca7-121">Kullanıcının soyadını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1fca7-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="1fca7-122">Bu parametre 1-100 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="1fca7-122">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="1fca7-123">Not</span><span class="sxs-lookup"><span data-stu-id="1fca7-123">-Note</span></span>
<span data-ttu-id="1fca7-124">Kullanıcı hakkında bir Not belirtir.</span><span class="sxs-lookup"><span data-stu-id="1fca7-124">Specifies a note about the user.</span></span>
<span data-ttu-id="1fca7-125">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="1fca7-125">This parameter is optional.</span></span>
<span data-ttu-id="1fca7-126">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="1fca7-126">The default value is $Null.</span></span>

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

### <span data-ttu-id="1fca7-127">-Parola</span><span class="sxs-lookup"><span data-stu-id="1fca7-127">-Password</span></span>
<span data-ttu-id="1fca7-128">Kullanıcı parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1fca7-128">Specifies the user password.</span></span>
<span data-ttu-id="1fca7-129">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="1fca7-129">This parameter is required.</span></span>

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

### <span data-ttu-id="1fca7-130">Durumlu</span><span class="sxs-lookup"><span data-stu-id="1fca7-130">-State</span></span>
<span data-ttu-id="1fca7-131">Kullanıcı durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1fca7-131">Specifies the user state.</span></span>
<span data-ttu-id="1fca7-132">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="1fca7-132">This parameter is optional.</span></span>
<span data-ttu-id="1fca7-133">Bu parametrenin varsayılan değeri $Null.</span><span class="sxs-lookup"><span data-stu-id="1fca7-133">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="1fca7-134">-UserID</span><span class="sxs-lookup"><span data-stu-id="1fca7-134">-UserId</span></span>
<span data-ttu-id="1fca7-135">Kullanıcı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1fca7-135">Specifies the user ID.</span></span>
<span data-ttu-id="1fca7-136">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="1fca7-136">This parameter is optional.</span></span>
<span data-ttu-id="1fca7-137">Bu parametre belirtilmezse, bu cmdlet bir kullanıcı KIMLIĞI oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1fca7-137">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

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

### <span data-ttu-id="1fca7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fca7-138">CommonParameters</span></span>
<span data-ttu-id="1fca7-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1fca7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fca7-140">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1fca7-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fca7-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1fca7-141">INPUTS</span></span>

### <span data-ttu-id="1fca7-142">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="1fca7-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1fca7-143">System. String</span><span class="sxs-lookup"><span data-stu-id="1fca7-143">System.String</span></span>

### <span data-ttu-id="1fca7-144">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="1fca7-144">System.Security.SecureString</span></span>

### <span data-ttu-id="1fca7-145">System. Nullable ' 1 [[Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementuserstate, Microsoft. Azure. PowerShell. cmdlet</span><span class="sxs-lookup"><span data-stu-id="1fca7-145">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="1fca7-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1fca7-146">OUTPUTS</span></span>

### <span data-ttu-id="1fca7-147">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementuser</span><span class="sxs-lookup"><span data-stu-id="1fca7-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="1fca7-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1fca7-148">NOTES</span></span>

## <span data-ttu-id="1fca7-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1fca7-149">RELATED LINKS</span></span>

[<span data-ttu-id="1fca7-150">Get-Azsız Kullanıcı</span><span class="sxs-lookup"><span data-stu-id="1fca7-150">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="1fca7-151">Set-Azapsananagementuser</span><span class="sxs-lookup"><span data-stu-id="1fca7-151">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


