---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementuserssourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUserSsoUrl.md
ms.openlocfilehash: 485150470bce308d3ab6d1a9a70eabd887abab09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591471"
---
# <span data-ttu-id="08210-101">Get-AzureRmApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="08210-101">Get-AzureRmApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="08210-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08210-102">SYNOPSIS</span></span>
<span data-ttu-id="08210-103">Kullanıcı için SSO URL 'SI oluşturur.</span><span class="sxs-lookup"><span data-stu-id="08210-103">Generates an SSO URL for a user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08210-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="08210-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08210-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="08210-105">DESCRIPTION</span></span>
<span data-ttu-id="08210-106">**Get-Azurermapsananagementuserssourl** cmdlet 'i, Kullanıcı için çoklu oturum açma (SSO) URL 'si oluşturur.</span><span class="sxs-lookup"><span data-stu-id="08210-106">The **Get-AzureRmApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="08210-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="08210-107">EXAMPLES</span></span>

### <span data-ttu-id="08210-108">Örnek 1: kullanıcının SSO URL 'sini alma</span><span class="sxs-lookup"><span data-stu-id="08210-108">Example 1: Get a user's SSO URL</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="08210-109">Bu komut bir kullanıcının SSO URL 'sini alır.</span><span class="sxs-lookup"><span data-stu-id="08210-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="08210-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="08210-110">PARAMETERS</span></span>

### <span data-ttu-id="08210-111">-Context</span><span class="sxs-lookup"><span data-stu-id="08210-111">-Context</span></span>
<span data-ttu-id="08210-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="08210-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="08210-113">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="08210-113">This parameter is required.</span></span>

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

### <span data-ttu-id="08210-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08210-114">-DefaultProfile</span></span>
<span data-ttu-id="08210-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="08210-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08210-116">-UserID</span><span class="sxs-lookup"><span data-stu-id="08210-116">-UserId</span></span>
<span data-ttu-id="08210-117">Bir kullanıcı KIMLIĞI belirtir.</span><span class="sxs-lookup"><span data-stu-id="08210-117">Specifies a user ID.</span></span>
<span data-ttu-id="08210-118">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="08210-118">This parameter is required.</span></span>

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

### <span data-ttu-id="08210-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08210-119">CommonParameters</span></span>
<span data-ttu-id="08210-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="08210-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08210-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08210-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08210-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="08210-122">INPUTS</span></span>

### <span data-ttu-id="08210-123">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="08210-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="08210-124">System. String</span><span class="sxs-lookup"><span data-stu-id="08210-124">System.String</span></span>

## <span data-ttu-id="08210-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="08210-125">OUTPUTS</span></span>

### <span data-ttu-id="08210-126">System. String</span><span class="sxs-lookup"><span data-stu-id="08210-126">System.String</span></span>

## <span data-ttu-id="08210-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="08210-127">NOTES</span></span>

## <span data-ttu-id="08210-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="08210-128">RELATED LINKS</span></span>

[<span data-ttu-id="08210-129">Get-Azurermapımanagementuser</span><span class="sxs-lookup"><span data-stu-id="08210-129">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)


