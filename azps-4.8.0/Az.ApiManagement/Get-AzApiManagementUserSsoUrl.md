---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementuserssourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUserSsoUrl.md
ms.openlocfilehash: be30497c444d90b9239b5dc3dcd351fbe9a63f0b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108004"
---
# <span data-ttu-id="e642f-101">Get-AzApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="e642f-101">Get-AzApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="e642f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e642f-102">SYNOPSIS</span></span>
<span data-ttu-id="e642f-103">Kullanıcı için SSO URL 'SI oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e642f-103">Generates an SSO URL for a user.</span></span>

## <span data-ttu-id="e642f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e642f-104">SYNTAX</span></span>

```
Get-AzApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e642f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e642f-105">DESCRIPTION</span></span>
<span data-ttu-id="e642f-106">**Get-Azapsananagementuserssourl** cmdlet 'i, Kullanıcı için çoklu oturum açma (SSO) URL 'si oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e642f-106">The **Get-AzApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="e642f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e642f-107">EXAMPLES</span></span>

### <span data-ttu-id="e642f-108">Örnek 1: kullanıcının SSO URL 'sini alma</span><span class="sxs-lookup"><span data-stu-id="e642f-108">Example 1: Get a user's SSO URL</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="e642f-109">Bu komut bir kullanıcının SSO URL 'sini alır.</span><span class="sxs-lookup"><span data-stu-id="e642f-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="e642f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e642f-110">PARAMETERS</span></span>

### <span data-ttu-id="e642f-111">-Context</span><span class="sxs-lookup"><span data-stu-id="e642f-111">-Context</span></span>
<span data-ttu-id="e642f-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e642f-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="e642f-113">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="e642f-113">This parameter is required.</span></span>

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

### <span data-ttu-id="e642f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e642f-114">-DefaultProfile</span></span>
<span data-ttu-id="e642f-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e642f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e642f-116">-UserID</span><span class="sxs-lookup"><span data-stu-id="e642f-116">-UserId</span></span>
<span data-ttu-id="e642f-117">Bir kullanıcı KIMLIĞI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e642f-117">Specifies a user ID.</span></span>
<span data-ttu-id="e642f-118">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="e642f-118">This parameter is required.</span></span>

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

### <span data-ttu-id="e642f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e642f-119">CommonParameters</span></span>
<span data-ttu-id="e642f-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e642f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e642f-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e642f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e642f-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e642f-122">INPUTS</span></span>

### <span data-ttu-id="e642f-123">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="e642f-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e642f-124">System. String</span><span class="sxs-lookup"><span data-stu-id="e642f-124">System.String</span></span>

## <span data-ttu-id="e642f-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e642f-125">OUTPUTS</span></span>

### <span data-ttu-id="e642f-126">System. String</span><span class="sxs-lookup"><span data-stu-id="e642f-126">System.String</span></span>

## <span data-ttu-id="e642f-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e642f-127">NOTES</span></span>

## <span data-ttu-id="e642f-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e642f-128">RELATED LINKS</span></span>

[<span data-ttu-id="e642f-129">Get-Azsız Kullanıcı</span><span class="sxs-lookup"><span data-stu-id="e642f-129">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


