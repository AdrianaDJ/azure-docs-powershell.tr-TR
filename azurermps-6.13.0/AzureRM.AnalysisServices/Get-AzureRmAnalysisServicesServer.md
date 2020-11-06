---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/get-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Get-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Get-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: efd4c4770bb9a2628530f476d44e9774534ceee7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589623"
---
# <span data-ttu-id="8764b-101">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="8764b-101">Get-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="8764b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8764b-102">SYNOPSIS</span></span>
<span data-ttu-id="8764b-103">Analysis Services sunucusunun ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="8764b-103">Gets the details of an Analysis Services server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8764b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8764b-104">SYNTAX</span></span>

```
Get-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8764b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8764b-105">DESCRIPTION</span></span>
<span data-ttu-id="8764b-106">Get-AzureRmAnalysisServicesServer cmdlet 'i Analysis Services sunucusunun ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="8764b-106">The Get-AzureRmAnalysisServicesServer cmdlet gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="8764b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8764b-107">EXAMPLES</span></span>

### <span data-ttu-id="8764b-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8764b-108">Example 1</span></span>
```
PS C:\>Get-AzureRmAnalysisServicesServer -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="8764b-109">Bu komut, ResourceGroup03 adındaki kaynak grubundaki tüm Azure Analysis Services sunucularını alır.</span><span class="sxs-lookup"><span data-stu-id="8764b-109">This command gets all Azure Analysis Services servers in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="8764b-110">Örnek 2: sunucu edinme</span><span class="sxs-lookup"><span data-stu-id="8764b-110">Example 2: Get a server</span></span>
```
PS C:\>Get-AzureRmAnalysisServicesServer -ResourceGroupName "ResourceGroup03" -Name "testserver"
```

<span data-ttu-id="8764b-111">Bu komut, ResourceGroup03 adlı kaynak grubunda TestServer adlı Azure Analysis Services sunucusunu alır.</span><span class="sxs-lookup"><span data-stu-id="8764b-111">This command gets the Azure Analysis Services server named testserver in the resource group named ResourceGroup03.</span></span>

## <span data-ttu-id="8764b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8764b-112">PARAMETERS</span></span>

### <span data-ttu-id="8764b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8764b-113">-DefaultProfile</span></span>
<span data-ttu-id="8764b-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8764b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8764b-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="8764b-115">-Name</span></span>
<span data-ttu-id="8764b-116">Analysis Services sunucusunun adı</span><span class="sxs-lookup"><span data-stu-id="8764b-116">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="8764b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8764b-117">-ResourceGroupName</span></span>
<span data-ttu-id="8764b-118">Sunucunun ait olduğu Azure Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="8764b-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="8764b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8764b-119">CommonParameters</span></span>
<span data-ttu-id="8764b-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8764b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8764b-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8764b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8764b-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8764b-122">INPUTS</span></span>

### <span data-ttu-id="8764b-123">System. String</span><span class="sxs-lookup"><span data-stu-id="8764b-123">System.String</span></span>

## <span data-ttu-id="8764b-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8764b-124">OUTPUTS</span></span>

### <span data-ttu-id="8764b-125">Microsoft. Azure. Commands. AnalysisServices. modeller. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="8764b-125">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="8764b-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8764b-126">NOTES</span></span>
<span data-ttu-id="8764b-127">Diğer ad: Get-AzureAs</span><span class="sxs-lookup"><span data-stu-id="8764b-127">Alias: Get-AzureAs</span></span>

## <span data-ttu-id="8764b-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8764b-128">RELATED LINKS</span></span>

[<span data-ttu-id="8764b-129">New-AzureRmAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="8764b-129">New-AzureRmAnalysisServicesServer </span></span>](./New-AzureRmAnalysisServicesServer .md)

[<span data-ttu-id="8764b-130">Remove-AzureRmAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="8764b-130">Remove-AzureRmAnalysisServicesServer </span></span>](./Remove-AzureRmAnalysisServicesServer .md)
