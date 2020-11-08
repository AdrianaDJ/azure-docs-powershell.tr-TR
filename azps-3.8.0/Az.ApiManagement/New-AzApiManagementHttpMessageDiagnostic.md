---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementhttpmessagediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementHttpMessageDiagnostic.md
ms.openlocfilehash: d3706168a23a32d4338069cb593ef8dd71242896
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097718"
---
# <span data-ttu-id="75341-101">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="75341-101">New-AzApiManagementHttpMessageDiagnostic</span></span>

## <span data-ttu-id="75341-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75341-102">SYNOPSIS</span></span>
<span data-ttu-id="75341-103">**PsApiManagementHttpMessageDiagnostic** 'In bir HTTP ileti tanı ayarı olan bir örneğini oluşturur</span><span class="sxs-lookup"><span data-stu-id="75341-103">Creates an instance of **PsApiManagementHttpMessageDiagnostic** which is an Http Message diagnostic setting of the Diagnostic</span></span>

## <span data-ttu-id="75341-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="75341-104">SYNTAX</span></span>

```
New-AzApiManagementHttpMessageDiagnostic [-HeadersToLog <String[]>] [-BodyBytesToLog <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75341-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="75341-105">DESCRIPTION</span></span>
<span data-ttu-id="75341-106">**New-AzApiManagementHttpMessageDiagnostic** cmdlet 'ı http ileti tanı ayarını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="75341-106">The cmdlet **New-AzApiManagementHttpMessageDiagnostic** creates the Http Message diagnostic setting.</span></span>

## <span data-ttu-id="75341-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="75341-107">EXAMPLES</span></span>

### <span data-ttu-id="75341-108">Örnek 1: temel bir http Ileti tanılama ayarı oluşturma</span><span class="sxs-lookup"><span data-stu-id="75341-108">Example 1 : Create a Basic Http Message diagnostic Setting</span></span>
```powershell
PS C:\>  New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100

Headers                   Body
-------                   ----
{Content-Type, UserAgent} Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBodyDiagnosticSetting
```

<span data-ttu-id="75341-109">`Content-Type`100 baytı ile birlikte günlüğe kaydetmek ve üstbilgiler için bir HTTP iletisi tanılama ayarı oluşturma `User-Agent``body`</span><span class="sxs-lookup"><span data-stu-id="75341-109">Create a http message diagnostic setting to log `Content-Type` and `User-Agent` headers along with 100 bytes of `body`</span></span>

## <span data-ttu-id="75341-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="75341-110">PARAMETERS</span></span>

### <span data-ttu-id="75341-111">-BodyBytesToLog</span><span class="sxs-lookup"><span data-stu-id="75341-111">-BodyBytesToLog</span></span>
<span data-ttu-id="75341-112">Günlüğe kaydedilecek istek gövdesi bayt sayısı.</span><span class="sxs-lookup"><span data-stu-id="75341-112">Number of request body bytes to log.</span></span> <span data-ttu-id="75341-113">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="75341-113">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75341-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75341-114">-DefaultProfile</span></span>
<span data-ttu-id="75341-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="75341-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75341-116">-HeadersToLog</span><span class="sxs-lookup"><span data-stu-id="75341-116">-HeadersToLog</span></span>
<span data-ttu-id="75341-117">Üst bilgi dizisi günlüğe yazılır.</span><span class="sxs-lookup"><span data-stu-id="75341-117">The array of headers to log.</span></span> <span data-ttu-id="75341-118">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="75341-118">This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75341-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75341-119">CommonParameters</span></span>
<span data-ttu-id="75341-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="75341-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75341-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="75341-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75341-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="75341-122">INPUTS</span></span>

### <span data-ttu-id="75341-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="75341-123">None</span></span>

## <span data-ttu-id="75341-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="75341-124">OUTPUTS</span></span>

### <span data-ttu-id="75341-125">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="75341-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic</span></span>

## <span data-ttu-id="75341-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="75341-126">NOTES</span></span>

## <span data-ttu-id="75341-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="75341-127">RELATED LINKS</span></span>

[<span data-ttu-id="75341-128">Yeni-Azsız</span><span class="sxs-lookup"><span data-stu-id="75341-128">New-AzApiManagementDiagnostic</span></span>](./New-AzApiManagementDiagnostic.md)

[<span data-ttu-id="75341-129">Yeni-Azapsanana,</span><span class="sxs-lookup"><span data-stu-id="75341-129">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)