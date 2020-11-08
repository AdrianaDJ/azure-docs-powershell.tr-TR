---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
ms.openlocfilehash: 060f58bc0206ea02f17239b6787f3a854aa3cb94
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107999"
---
# <span data-ttu-id="e6ed7-101">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e6ed7-101">New-AzApiManagementContext</span></span>

## <span data-ttu-id="e6ed7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6ed7-102">SYNOPSIS</span></span>
<span data-ttu-id="e6ed7-103">Psazureapsananagementcontext örneği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e6ed7-103">Creates an instance of PsAzureApiManagementContext.</span></span>

## <span data-ttu-id="e6ed7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e6ed7-104">SYNTAX</span></span>

### <span data-ttu-id="e6ed7-105">ContextParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e6ed7-105">ContextParameterSet (Default)</span></span>
```
New-AzApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6ed7-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="e6ed7-106">ResourceIdParameterSet</span></span>
```
New-AzApiManagementContext -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6ed7-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e6ed7-107">DESCRIPTION</span></span>
<span data-ttu-id="e6ed7-108">**Yeni-azapsananagementcontext** cmdlet 'ı **Psazureapsananagementcontext** örneği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e6ed7-108">The **New-AzApiManagementContext** cmdlet creates an instance of **PsAzureApiManagementContext**.</span></span>
<span data-ttu-id="e6ed7-109">Bağlam, API yönetim hizmeti cmdlet 'lerinin tümü için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e6ed7-109">The context is used for all of the API Management service cmdlets.</span></span>

## <span data-ttu-id="e6ed7-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e6ed7-110">EXAMPLES</span></span>

### <span data-ttu-id="e6ed7-111">Örnek 1: Psapsananagementcontext örneği oluşturma</span><span class="sxs-lookup"><span data-stu-id="e6ed7-111">Example 1: Create a PsApiManagementContext instance</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

<span data-ttu-id="e6ed7-112">Bu komut bir **Psapsananagementcontext** örneği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e6ed7-112">This command creates an instance of **PsApiManagementContext**.</span></span>

## <span data-ttu-id="e6ed7-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e6ed7-113">PARAMETERS</span></span>

### <span data-ttu-id="e6ed7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6ed7-114">-DefaultProfile</span></span>
<span data-ttu-id="e6ed7-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e6ed7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6ed7-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6ed7-116">-ResourceGroupName</span></span>
<span data-ttu-id="e6ed7-117">API yönetim hizmetinin dağıtıldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6ed7-117">Specifies the name of the resource group under which an API Management service is deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6ed7-118">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e6ed7-118">-ResourceId</span></span>
<span data-ttu-id="e6ed7-119">Bir anlık hizmetin ARM kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="e6ed7-119">Arm Resource Identifier of a ApiManagement service.</span></span> <span data-ttu-id="e6ed7-120">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="e6ed7-120">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6ed7-121">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="e6ed7-121">-ServiceName</span></span>
<span data-ttu-id="e6ed7-122">Dağıtılmış API yönetim hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6ed7-122">Specifies the name of the deployed API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6ed7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6ed7-123">CommonParameters</span></span>
<span data-ttu-id="e6ed7-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e6ed7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6ed7-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e6ed7-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6ed7-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e6ed7-126">INPUTS</span></span>

### <span data-ttu-id="e6ed7-127">System. String</span><span class="sxs-lookup"><span data-stu-id="e6ed7-127">System.String</span></span>

## <span data-ttu-id="e6ed7-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e6ed7-128">OUTPUTS</span></span>

### <span data-ttu-id="e6ed7-129">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="e6ed7-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="e6ed7-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e6ed7-130">NOTES</span></span>

## <span data-ttu-id="e6ed7-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e6ed7-131">RELATED LINKS</span></span>
