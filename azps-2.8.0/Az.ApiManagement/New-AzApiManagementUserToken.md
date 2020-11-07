---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementusertoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUserToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementUserToken.md
ms.openlocfilehash: 71f4960dce883b809d9ee9c5bc7011d8ab04c5bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753494"
---
# <span data-ttu-id="3918e-101">New-AzApiManagementUserToken</span><span class="sxs-lookup"><span data-stu-id="3918e-101">New-AzApiManagementUserToken</span></span>

## <span data-ttu-id="3918e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3918e-102">SYNOPSIS</span></span>
<span data-ttu-id="3918e-103">Kullanıcı için paylaşılan bir erişim belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3918e-103">Generates a Shared Access Token for the User.</span></span>

## <span data-ttu-id="3918e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3918e-104">SYNTAX</span></span>

```
New-AzApiManagementUserToken -Context <PsApiManagementContext> -UserId <String>
 [-KeyType <PsApiManagementUserKeyType>] [-Expiry <DateTime>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3918e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3918e-105">DESCRIPTION</span></span>
<span data-ttu-id="3918e-106">**New-Azapsananagementusertoken** cmdlet 'i, belirli bir Kullanıcı Için paylaşılan erişim belirteci oluşturur</span><span class="sxs-lookup"><span data-stu-id="3918e-106">The cmdlet **New-AzApiManagementUserToken** generates a Shared Access Token for a specified User</span></span>

## <span data-ttu-id="3918e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3918e-107">EXAMPLES</span></span>

### <span data-ttu-id="3918e-108">Örnek 1: git kullanıcısı için paylaşılan erişim belirteci oluşturma</span><span class="sxs-lookup"><span data-stu-id="3918e-108">Example 1 : Generate a Shared Access Token for Git User</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceGroupName powershelltest -ServiceName
powershellsdkservice
S D:\github\azure-powershell> $gitAccess=Get-AzApiManagementTenantAccess -Context $context
PS D:\github\azure-powershell> New-AzApiManagementUserToken -Context $context -UserId $gitAccess.Id

UserId      TokenExpiry         KeyType UserToken
------      -----------         ------- ---------
integration 5/3/2019 2:02:34 PM Primary integration&201905031402&zOwopJChWAA6oaqGHMyf7Ol9wUCPcrtdmBmff8c2lcmZk9Y...
```

<span data-ttu-id="3918e-109">Bu komut dosyası, Apımanaıla hizmetinde yapılandırılmış git kullanıcısını alır ve birincil anahtarı 8 saat geçerli kullanarak bir paylaşılan erişim belirteci oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3918e-109">This script get the Git user configured in ApiManagement service and generates a Shared Access Token using the Primary Key valid for 8 hours.</span></span>

## <span data-ttu-id="3918e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3918e-110">PARAMETERS</span></span>

### <span data-ttu-id="3918e-111">-Context</span><span class="sxs-lookup"><span data-stu-id="3918e-111">-Context</span></span>
<span data-ttu-id="3918e-112">Psapsananagementcontext örneği.</span><span class="sxs-lookup"><span data-stu-id="3918e-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="3918e-113">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="3918e-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3918e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3918e-114">-DefaultProfile</span></span>
<span data-ttu-id="3918e-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3918e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3918e-116">-Süre sonu</span><span class="sxs-lookup"><span data-stu-id="3918e-116">-Expiry</span></span>
<span data-ttu-id="3918e-117">Simgenin süre sonu.</span><span class="sxs-lookup"><span data-stu-id="3918e-117">Expiry of the Token.</span></span>
<span data-ttu-id="3918e-118">Belirtilmezse, belirteç 8 saat sonra sona erecek şekilde oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="3918e-118">If not specified, the token is created to expire after 8 hours.</span></span>
<span data-ttu-id="3918e-119">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="3918e-119">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3918e-120">-KeyType</span><span class="sxs-lookup"><span data-stu-id="3918e-120">-KeyType</span></span>
<span data-ttu-id="3918e-121">Belirteç oluştururken kullanılacak kullanıcı anahtarı.</span><span class="sxs-lookup"><span data-stu-id="3918e-121">User Key to use when generating the Token.</span></span>
<span data-ttu-id="3918e-122">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="3918e-122">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserKeyType
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3918e-123">-UserID</span><span class="sxs-lookup"><span data-stu-id="3918e-123">-UserId</span></span>
<span data-ttu-id="3918e-124">Var olan kullanıcının tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="3918e-124">Identifier of existing user.</span></span>
<span data-ttu-id="3918e-125">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="3918e-125">This parameter is required.</span></span>

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

### <span data-ttu-id="3918e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3918e-126">CommonParameters</span></span>
<span data-ttu-id="3918e-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3918e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3918e-128">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3918e-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3918e-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3918e-129">INPUTS</span></span>

### <span data-ttu-id="3918e-130">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="3918e-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3918e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="3918e-131">System.String</span></span>

### <span data-ttu-id="3918e-132">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementuserkeytype</span><span class="sxs-lookup"><span data-stu-id="3918e-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserKeyType</span></span>

### <span data-ttu-id="3918e-133">System. Nullable ' 1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="3918e-133">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="3918e-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3918e-134">OUTPUTS</span></span>

### <span data-ttu-id="3918e-135">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementusertoken</span><span class="sxs-lookup"><span data-stu-id="3918e-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserToken</span></span>

## <span data-ttu-id="3918e-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3918e-136">NOTES</span></span>

## <span data-ttu-id="3918e-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3918e-137">RELATED LINKS</span></span>
