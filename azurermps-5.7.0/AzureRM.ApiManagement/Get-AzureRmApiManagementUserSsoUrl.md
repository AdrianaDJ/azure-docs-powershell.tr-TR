---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 27FF1B7D-E103-4504-AD09-8D3A8BCA8B75
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementuserssourl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUserSsoUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUserSsoUrl.md
ms.openlocfilehash: 5cc7eb81c9ccaf461b1f2ab16e76aa662ea0f57b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589912"
---
# <span data-ttu-id="64f7f-101">Get-AzureRmApiManagementUserSsoUrl</span><span class="sxs-lookup"><span data-stu-id="64f7f-101">Get-AzureRmApiManagementUserSsoUrl</span></span>

## <span data-ttu-id="64f7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64f7f-102">SYNOPSIS</span></span>
<span data-ttu-id="64f7f-103">Kullanıcı için SSO URL 'SI oluşturur.</span><span class="sxs-lookup"><span data-stu-id="64f7f-103">Generates an SSO URL for a user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64f7f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="64f7f-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementUserSsoUrl -Context <PsApiManagementContext> -UserId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64f7f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="64f7f-105">DESCRIPTION</span></span>
<span data-ttu-id="64f7f-106">**Get-Azurermapsananagementuserssourl** cmdlet 'i, Kullanıcı için çoklu oturum açma (SSO) URL 'si oluşturur.</span><span class="sxs-lookup"><span data-stu-id="64f7f-106">The **Get-AzureRmApiManagementUserSsoUrl** cmdlet generates a single sign-on (SSO) URL for a user.</span></span>

## <span data-ttu-id="64f7f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="64f7f-107">EXAMPLES</span></span>

### <span data-ttu-id="64f7f-108">Örnek 1: kullanıcının SSO URL 'sini alma</span><span class="sxs-lookup"><span data-stu-id="64f7f-108">Example 1: Get a user's SSO URL</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementUserSsoUrl -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="64f7f-109">Bu komut bir kullanıcının SSO URL 'sini alır.</span><span class="sxs-lookup"><span data-stu-id="64f7f-109">This command gets a user's SSO URL.</span></span>

## <span data-ttu-id="64f7f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="64f7f-110">PARAMETERS</span></span>

### <span data-ttu-id="64f7f-111">-Context</span><span class="sxs-lookup"><span data-stu-id="64f7f-111">-Context</span></span>
<span data-ttu-id="64f7f-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="64f7f-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="64f7f-113">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="64f7f-113">This parameter is required.</span></span>

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

### <span data-ttu-id="64f7f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64f7f-114">-DefaultProfile</span></span>
<span data-ttu-id="64f7f-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="64f7f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64f7f-116">-UserID</span><span class="sxs-lookup"><span data-stu-id="64f7f-116">-UserId</span></span>
<span data-ttu-id="64f7f-117">Bir kullanıcı KIMLIĞI belirtir.</span><span class="sxs-lookup"><span data-stu-id="64f7f-117">Specifies a user ID.</span></span>
<span data-ttu-id="64f7f-118">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="64f7f-118">This parameter is required.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64f7f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64f7f-119">CommonParameters</span></span>
<span data-ttu-id="64f7f-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="64f7f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64f7f-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64f7f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64f7f-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="64f7f-122">INPUTS</span></span>

### <span data-ttu-id="64f7f-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="64f7f-123">None</span></span>
<span data-ttu-id="64f7f-124">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="64f7f-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="64f7f-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="64f7f-125">OUTPUTS</span></span>

### <span data-ttu-id="64f7f-126">dizisi</span><span class="sxs-lookup"><span data-stu-id="64f7f-126">string</span></span>

## <span data-ttu-id="64f7f-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="64f7f-127">NOTES</span></span>

## <span data-ttu-id="64f7f-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="64f7f-128">RELATED LINKS</span></span>

[<span data-ttu-id="64f7f-129">Get-Azurermapımanagementuser</span><span class="sxs-lookup"><span data-stu-id="64f7f-129">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)


