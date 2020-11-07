---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
ms.openlocfilehash: cec27d1f7fb83cb114cd4b9a5c508c807e8ebd5c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761675"
---
# <span data-ttu-id="6d809-101">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6d809-101">New-AzApiManagementContext</span></span>

## <span data-ttu-id="6d809-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d809-102">SYNOPSIS</span></span>
<span data-ttu-id="6d809-103">Psazureapsananagementcontext örneği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6d809-103">Creates an instance of PsAzureApiManagementContext.</span></span>

## <span data-ttu-id="6d809-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6d809-104">SYNTAX</span></span>

```
New-AzApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d809-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6d809-105">DESCRIPTION</span></span>
<span data-ttu-id="6d809-106">**Yeni-azapsananagementcontext** cmdlet 'ı **Psazureapsananagementcontext** örneği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6d809-106">The **New-AzApiManagementContext** cmdlet creates an instance of **PsAzureApiManagementContext**.</span></span>
<span data-ttu-id="6d809-107">Bağlam, API yönetim hizmeti cmdlet 'lerinin tümü için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6d809-107">The context is used for all of the API Management service cmdlets.</span></span>

## <span data-ttu-id="6d809-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6d809-108">EXAMPLES</span></span>

### <span data-ttu-id="6d809-109">Örnek 1: Psapsananagementcontext örneği oluşturma</span><span class="sxs-lookup"><span data-stu-id="6d809-109">Example 1: Create a PsApiManagementContext instance</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

<span data-ttu-id="6d809-110">Bu komut bir **Psapsananagementcontext** örneği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6d809-110">This command creates an instance of **PsApiManagementContext**.</span></span>

## <span data-ttu-id="6d809-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6d809-111">PARAMETERS</span></span>

### <span data-ttu-id="6d809-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d809-112">-DefaultProfile</span></span>
<span data-ttu-id="6d809-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6d809-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d809-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d809-114">-ResourceGroupName</span></span>
<span data-ttu-id="6d809-115">API yönetim hizmetinin dağıtıldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d809-115">Specifies the name of the resource group under which an API Management service is deployed.</span></span>

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

### <span data-ttu-id="6d809-116">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="6d809-116">-ServiceName</span></span>
<span data-ttu-id="6d809-117">Dağıtılmış API yönetim hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d809-117">Specifies the name of the deployed API Management service.</span></span>

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

### <span data-ttu-id="6d809-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d809-118">CommonParameters</span></span>
<span data-ttu-id="6d809-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6d809-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d809-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d809-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d809-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6d809-121">INPUTS</span></span>

### <span data-ttu-id="6d809-122">System. String</span><span class="sxs-lookup"><span data-stu-id="6d809-122">System.String</span></span>

## <span data-ttu-id="6d809-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6d809-123">OUTPUTS</span></span>

### <span data-ttu-id="6d809-124">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="6d809-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="6d809-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6d809-125">NOTES</span></span>

## <span data-ttu-id="6d809-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6d809-126">RELATED LINKS</span></span>
