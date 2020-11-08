---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/get-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Get-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Get-AzAnalysisServicesServer.md
ms.openlocfilehash: c0c308bfe9d2d5fad971f9df1a26b03710d5629c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096661"
---
# <span data-ttu-id="1f8cf-101">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="1f8cf-101">Get-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="1f8cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f8cf-102">SYNOPSIS</span></span>
<span data-ttu-id="1f8cf-103">Analysis Services sunucusunun ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="1f8cf-103">Gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="1f8cf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1f8cf-104">SYNTAX</span></span>

```
Get-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f8cf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1f8cf-105">DESCRIPTION</span></span>
<span data-ttu-id="1f8cf-106">Get-AzAnalysisServicesServer cmdlet 'i Analysis Services sunucusunun ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="1f8cf-106">The Get-AzAnalysisServicesServer cmdlet gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="1f8cf-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1f8cf-107">EXAMPLES</span></span>

### <span data-ttu-id="1f8cf-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1f8cf-108">Example 1</span></span>
```
PS C:\>Get-AzAnalysisServicesServer -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="1f8cf-109">Bu komut, ResourceGroup03 adındaki kaynak grubundaki tüm Azure Analysis Services sunucularını alır.</span><span class="sxs-lookup"><span data-stu-id="1f8cf-109">This command gets all Azure Analysis Services servers in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="1f8cf-110">Örnek 2: sunucu edinme</span><span class="sxs-lookup"><span data-stu-id="1f8cf-110">Example 2: Get a server</span></span>
```
PS C:\>Get-AzAnalysisServicesServer -ResourceGroupName "ResourceGroup03" -Name "testserver"
```

<span data-ttu-id="1f8cf-111">Bu komut, ResourceGroup03 adlı kaynak grubunda TestServer adlı Azure Analysis Services sunucusunu alır.</span><span class="sxs-lookup"><span data-stu-id="1f8cf-111">This command gets the Azure Analysis Services server named testserver in the resource group named ResourceGroup03.</span></span>

## <span data-ttu-id="1f8cf-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1f8cf-112">PARAMETERS</span></span>

### <span data-ttu-id="1f8cf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f8cf-113">-DefaultProfile</span></span>
<span data-ttu-id="1f8cf-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1f8cf-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f8cf-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="1f8cf-115">-Name</span></span>
<span data-ttu-id="1f8cf-116">Analysis Services sunucusunun adı</span><span class="sxs-lookup"><span data-stu-id="1f8cf-116">Name of the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f8cf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f8cf-117">-ResourceGroupName</span></span>
<span data-ttu-id="1f8cf-118">Sunucunun ait olduğu Azure Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="1f8cf-118">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f8cf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f8cf-119">CommonParameters</span></span>
<span data-ttu-id="1f8cf-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1f8cf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f8cf-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f8cf-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f8cf-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1f8cf-122">INPUTS</span></span>

### <span data-ttu-id="1f8cf-123">System. String</span><span class="sxs-lookup"><span data-stu-id="1f8cf-123">System.String</span></span>

## <span data-ttu-id="1f8cf-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1f8cf-124">OUTPUTS</span></span>

### <span data-ttu-id="1f8cf-125">Microsoft. Azure. Commands. AnalysisServices. modeller. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="1f8cf-125">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="1f8cf-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1f8cf-126">NOTES</span></span>
<span data-ttu-id="1f8cf-127">Diğer ad: Get-AzAs</span><span class="sxs-lookup"><span data-stu-id="1f8cf-127">Alias: Get-AzAs</span></span>

## <span data-ttu-id="1f8cf-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1f8cf-128">RELATED LINKS</span></span>

[<span data-ttu-id="1f8cf-129">Yeni-AzAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="1f8cf-129">New-AzAnalysisServicesServer </span></span>](./New-AzAnalysisServicesServer .md)

[<span data-ttu-id="1f8cf-130">Remove-AzAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="1f8cf-130">Remove-AzAnalysisServicesServer </span></span>](./Remove-AzAnalysisServicesServer .md)
