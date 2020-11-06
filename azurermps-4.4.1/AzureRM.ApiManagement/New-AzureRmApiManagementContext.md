---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementContext.md
ms.openlocfilehash: 7bf97454fd7dc4a2debc8861766981f6428f0b28
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591227"
---
# <span data-ttu-id="dbc03-101">New-AzureRmApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="dbc03-101">New-AzureRmApiManagementContext</span></span>

## <span data-ttu-id="dbc03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbc03-102">SYNOPSIS</span></span>
<span data-ttu-id="dbc03-103">Psazureapsananagementcontext örneği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dbc03-103">Creates an instance of PsAzureApiManagementContext.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dbc03-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dbc03-104">SYNTAX</span></span>

```
New-AzureRmApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbc03-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dbc03-105">DESCRIPTION</span></span>
<span data-ttu-id="dbc03-106">**New-Azurermapsananagementcontext** cmdlet 'ı **Psazureapsananagementcontext** örneği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dbc03-106">The **New-AzureRmApiManagementContext** cmdlet creates an instance of **PsAzureApiManagementContext**.</span></span>
<span data-ttu-id="dbc03-107">Bağlam, API yönetim hizmeti cmdlet 'lerinin tümü için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="dbc03-107">The context is used for all of the API Management service cmdlets.</span></span>

## <span data-ttu-id="dbc03-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dbc03-108">EXAMPLES</span></span>

### <span data-ttu-id="dbc03-109">Örnek 1: Psapsananagementcontext örneği oluşturma</span><span class="sxs-lookup"><span data-stu-id="dbc03-109">Example 1: Create a PsApiManagementContext instance</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

<span data-ttu-id="dbc03-110">Bu komut bir **Psapsananagementcontext** örneği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dbc03-110">This command creates an instance of **PsApiManagementContext**.</span></span>

## <span data-ttu-id="dbc03-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dbc03-111">PARAMETERS</span></span>

### <span data-ttu-id="dbc03-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbc03-112">-ResourceGroupName</span></span>
<span data-ttu-id="dbc03-113">API yönetim hizmetinin dağıtıldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dbc03-113">Specifies the name of the resource group under which an API Management service is deployed.</span></span>

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

### <span data-ttu-id="dbc03-114">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="dbc03-114">-ServiceName</span></span>
<span data-ttu-id="dbc03-115">Dağıtılmış API yönetim hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dbc03-115">Specifies the name of the deployed API Management service.</span></span>

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

### <span data-ttu-id="dbc03-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbc03-116">-DefaultProfile</span></span>
<span data-ttu-id="dbc03-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dbc03-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbc03-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbc03-118">CommonParameters</span></span>
<span data-ttu-id="dbc03-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dbc03-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbc03-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbc03-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbc03-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dbc03-121">INPUTS</span></span>

## <span data-ttu-id="dbc03-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dbc03-122">OUTPUTS</span></span>

### <span data-ttu-id="dbc03-123">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psazureapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="dbc03-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsAzureApiManagementContext</span></span>

## <span data-ttu-id="dbc03-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dbc03-124">NOTES</span></span>

## <span data-ttu-id="dbc03-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dbc03-125">RELATED LINKS</span></span>

