---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 3C467F64-7525-4420-9AFE-DCB98EF6D203
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementUser.md
ms.openlocfilehash: 1c8b7f8069c63d18f69285f7e40ac4d652f0bf73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762497"
---
# <span data-ttu-id="9ccc5-101">New-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="9ccc5-101">New-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="9ccc5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ccc5-102">SYNOPSIS</span></span>
<span data-ttu-id="9ccc5-103">Yeni bir kullanıcı kaydeder.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-103">Registers a new user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ccc5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9ccc5-104">SYNTAX</span></span>

```
New-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>] -FirstName <String>
 -LastName <String> -Email <String> -Password <SecureString> [-State <PsApiManagementUserState>]
 [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ccc5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9ccc5-105">DESCRIPTION</span></span>
<span data-ttu-id="9ccc5-106">**Yeni-Azurermapsananagementuser** cmdlet 'i yeni bir kullanıcı kaydeder.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-106">The **New-AzureRmApiManagementUser** cmdlet registers a new user.</span></span>

## <span data-ttu-id="9ccc5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9ccc5-107">EXAMPLES</span></span>

### <span data-ttu-id="9ccc5-108">Örnek 1: yeni bir kullanıcıyı kaydettirme</span><span class="sxs-lookup"><span data-stu-id="9ccc5-108">Example 1: Register a new user</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$securePassword = ConvertTo-SecureString "qwerty" -AsPlainText -Force
PS C:\>New-AzureRmApiManagementUser -Context $apimContext -FirstName "Patti" -LastName "Fuller" -Email "Patti.Fuller@contoso.com" -Password $securePassword
```

<span data-ttu-id="9ccc5-109">Bu komut, Patti Fuller adlı yeni bir kullanıcı kaydeder.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-109">This command registers a new user named Patti Fuller.</span></span>

## <span data-ttu-id="9ccc5-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9ccc5-110">PARAMETERS</span></span>

### <span data-ttu-id="9ccc5-111">-Context</span><span class="sxs-lookup"><span data-stu-id="9ccc5-111">-Context</span></span>
<span data-ttu-id="9ccc5-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="9ccc5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ccc5-113">-DefaultProfile</span></span>
<span data-ttu-id="9ccc5-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ccc5-115">-E-posta</span><span class="sxs-lookup"><span data-stu-id="9ccc5-115">-Email</span></span>
<span data-ttu-id="9ccc5-116">Kullanıcının e-posta adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-116">Specifies the email address of the user.</span></span>

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

### <span data-ttu-id="9ccc5-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="9ccc5-117">-FirstName</span></span>
<span data-ttu-id="9ccc5-118">Kullanıcının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-118">Specifies the first name of the user.</span></span>
<span data-ttu-id="9ccc5-119">Bu parametre 1-100 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-119">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="9ccc5-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="9ccc5-120">-LastName</span></span>
<span data-ttu-id="9ccc5-121">Kullanıcının soyadını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-121">Specifies the last name of the user.</span></span>
<span data-ttu-id="9ccc5-122">Bu parametre 1-100 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-122">This parameter must be 1 to 100 characters long.</span></span>

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

### <span data-ttu-id="9ccc5-123">Not</span><span class="sxs-lookup"><span data-stu-id="9ccc5-123">-Note</span></span>
<span data-ttu-id="9ccc5-124">Kullanıcı hakkında bir Not belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-124">Specifies a note about the user.</span></span>
<span data-ttu-id="9ccc5-125">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-125">This parameter is optional.</span></span>
<span data-ttu-id="9ccc5-126">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-126">The default value is $Null.</span></span>

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

### <span data-ttu-id="9ccc5-127">-Parola</span><span class="sxs-lookup"><span data-stu-id="9ccc5-127">-Password</span></span>
<span data-ttu-id="9ccc5-128">Kullanıcı parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-128">Specifies the user password.</span></span>
<span data-ttu-id="9ccc5-129">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-129">This parameter is required.</span></span>

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

### <span data-ttu-id="9ccc5-130">Durumlu</span><span class="sxs-lookup"><span data-stu-id="9ccc5-130">-State</span></span>
<span data-ttu-id="9ccc5-131">Kullanıcı durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-131">Specifies the user state.</span></span>
<span data-ttu-id="9ccc5-132">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-132">This parameter is optional.</span></span>
<span data-ttu-id="9ccc5-133">Bu parametrenin varsayılan değeri $Null.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-133">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="9ccc5-134">-UserID</span><span class="sxs-lookup"><span data-stu-id="9ccc5-134">-UserId</span></span>
<span data-ttu-id="9ccc5-135">Kullanıcı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-135">Specifies the user ID.</span></span>
<span data-ttu-id="9ccc5-136">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-136">This parameter is optional.</span></span>
<span data-ttu-id="9ccc5-137">Bu parametre belirtilmezse, bu cmdlet bir kullanıcı KIMLIĞI oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-137">If this parameter is not specified, this cmdlet generates a user ID.</span></span>

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

### <span data-ttu-id="9ccc5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ccc5-138">CommonParameters</span></span>
<span data-ttu-id="9ccc5-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ccc5-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ccc5-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ccc5-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9ccc5-141">INPUTS</span></span>

### <span data-ttu-id="9ccc5-142">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="9ccc5-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9ccc5-143">System. String</span><span class="sxs-lookup"><span data-stu-id="9ccc5-143">System.String</span></span>

### <span data-ttu-id="9ccc5-144">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="9ccc5-144">System.Security.SecureString</span></span>

### <span data-ttu-id="9ccc5-145">System. Nullable ' 1 [[Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementuserstate, Microsoft. Azure. Commands</span><span class="sxs-lookup"><span data-stu-id="9ccc5-145">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState, Microsoft.Azure.Commands.ApiManagement.ServiceManagement, Version=6.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="9ccc5-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9ccc5-146">OUTPUTS</span></span>

### <span data-ttu-id="9ccc5-147">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementuser</span><span class="sxs-lookup"><span data-stu-id="9ccc5-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUser</span></span>

## <span data-ttu-id="9ccc5-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9ccc5-148">NOTES</span></span>

## <span data-ttu-id="9ccc5-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9ccc5-149">RELATED LINKS</span></span>

[<span data-ttu-id="9ccc5-150">Get-Azurermapımanagementuser</span><span class="sxs-lookup"><span data-stu-id="9ccc5-150">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="9ccc5-151">Set-Azurermapımanagementuser</span><span class="sxs-lookup"><span data-stu-id="9ccc5-151">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


