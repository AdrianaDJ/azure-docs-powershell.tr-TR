---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementContext.md
ms.openlocfilehash: da9924624065937a0cb2d78160b1a12cb698a42d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589910"
---
# <span data-ttu-id="7bb25-101">New-AzureRmApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7bb25-101">New-AzureRmApiManagementContext</span></span>

## <span data-ttu-id="7bb25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bb25-102">SYNOPSIS</span></span>
<span data-ttu-id="7bb25-103">Psazureapsananagementcontext örneği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7bb25-103">Creates an instance of PsAzureApiManagementContext.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7bb25-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7bb25-104">SYNTAX</span></span>

```
New-AzureRmApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7bb25-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7bb25-105">DESCRIPTION</span></span>
<span data-ttu-id="7bb25-106">**New-Azurermapsananagementcontext** cmdlet 'ı **Psazureapsananagementcontext** örneği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7bb25-106">The **New-AzureRmApiManagementContext** cmdlet creates an instance of **PsAzureApiManagementContext**.</span></span>
<span data-ttu-id="7bb25-107">Bağlam, API yönetim hizmeti cmdlet 'lerinin tümü için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7bb25-107">The context is used for all of the API Management service cmdlets.</span></span>

## <span data-ttu-id="7bb25-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7bb25-108">EXAMPLES</span></span>

### <span data-ttu-id="7bb25-109">Örnek 1: Psapsananagementcontext örneği oluşturma</span><span class="sxs-lookup"><span data-stu-id="7bb25-109">Example 1: Create a PsApiManagementContext instance</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

<span data-ttu-id="7bb25-110">Bu komut bir **Psapsananagementcontext** örneği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7bb25-110">This command creates an instance of **PsApiManagementContext**.</span></span>

## <span data-ttu-id="7bb25-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7bb25-111">PARAMETERS</span></span>

### <span data-ttu-id="7bb25-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bb25-112">-DefaultProfile</span></span>
<span data-ttu-id="7bb25-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7bb25-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="7bb25-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bb25-114">-ResourceGroupName</span></span>
<span data-ttu-id="7bb25-115">API yönetim hizmetinin dağıtıldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7bb25-115">Specifies the name of the resource group under which an API Management service is deployed.</span></span>

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

### <span data-ttu-id="7bb25-116">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="7bb25-116">-ServiceName</span></span>
<span data-ttu-id="7bb25-117">Dağıtılmış API yönetim hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7bb25-117">Specifies the name of the deployed API Management service.</span></span>

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

### <span data-ttu-id="7bb25-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bb25-118">CommonParameters</span></span>
<span data-ttu-id="7bb25-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7bb25-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bb25-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bb25-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bb25-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7bb25-121">INPUTS</span></span>

### <span data-ttu-id="7bb25-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7bb25-122">None</span></span>
<span data-ttu-id="7bb25-123">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="7bb25-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7bb25-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7bb25-124">OUTPUTS</span></span>

### <span data-ttu-id="7bb25-125">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psazureapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="7bb25-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsAzureApiManagementContext</span></span>

## <span data-ttu-id="7bb25-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7bb25-126">NOTES</span></span>

## <span data-ttu-id="7bb25-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7bb25-127">RELATED LINKS</span></span>

