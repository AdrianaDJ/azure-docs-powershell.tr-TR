---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Get-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Get-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: f80f3eead528c7731007bcd6611f5d6fecbb55e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588018"
---
# <span data-ttu-id="f1a7e-101">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="f1a7e-101">Get-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="f1a7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1a7e-102">SYNOPSIS</span></span>
<span data-ttu-id="f1a7e-103">Analysis Services sunucusunun ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="f1a7e-103">Gets the details of an Analysis Services server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1a7e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f1a7e-104">SYNTAX</span></span>

```
Get-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1a7e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f1a7e-105">DESCRIPTION</span></span>
<span data-ttu-id="f1a7e-106">Get-AzureRmAnalysisServicesServer cmdlet 'i Analysis Services sunucusunun ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="f1a7e-106">The Get-AzureRmAnalysisServicesServer cmdlet gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="f1a7e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f1a7e-107">EXAMPLES</span></span>

### <span data-ttu-id="f1a7e-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f1a7e-108">Example 1</span></span>
```
PS C:\>Get-AzureRmAnalysisServicesServer -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="f1a7e-109">Bu komut, ResourceGroup03 adındaki kaynak grubundaki tüm Azure Analysis Services sunucularını alır.</span><span class="sxs-lookup"><span data-stu-id="f1a7e-109">This command gets all Azure Analysis Services servers in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="f1a7e-110">Örnek 2: sunucu edinme</span><span class="sxs-lookup"><span data-stu-id="f1a7e-110">Example 2: Get a server</span></span>
```
PS C:\>Get-AzureRmAnalysisServicesServer -ResourceGroupName "ResourceGroup03" -Name "testserver"
```

<span data-ttu-id="f1a7e-111">Bu komut, ResourceGroup03 adlı kaynak grubunda TestServer adlı Azure Analysis Services sunucusunu alır.</span><span class="sxs-lookup"><span data-stu-id="f1a7e-111">This command gets the Azure Analysis Services server named testserver in the resource group named ResourceGroup03.</span></span>

## <span data-ttu-id="f1a7e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f1a7e-112">PARAMETERS</span></span>

### <span data-ttu-id="f1a7e-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="f1a7e-113">-Name</span></span>
<span data-ttu-id="f1a7e-114">Analysis Services sunucusunun adı</span><span class="sxs-lookup"><span data-stu-id="f1a7e-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="f1a7e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1a7e-115">-ResourceGroupName</span></span>
<span data-ttu-id="f1a7e-116">Sunucunun ait olduğu Azure Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="f1a7e-116">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="f1a7e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1a7e-117">-DefaultProfile</span></span>
<span data-ttu-id="f1a7e-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f1a7e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1a7e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1a7e-119">CommonParameters</span></span>
<span data-ttu-id="f1a7e-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f1a7e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1a7e-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1a7e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1a7e-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f1a7e-122">INPUTS</span></span>

## <span data-ttu-id="f1a7e-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f1a7e-123">OUTPUTS</span></span>

### <span data-ttu-id="f1a7e-124">Microsoft. Azure. Commands. AnalysisServices. modeller. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="f1a7e-124">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="f1a7e-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f1a7e-125">NOTES</span></span>
<span data-ttu-id="f1a7e-126">Diğer ad: Get-AzureAs</span><span class="sxs-lookup"><span data-stu-id="f1a7e-126">Alias: Get-AzureAs</span></span>

## <span data-ttu-id="f1a7e-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f1a7e-127">RELATED LINKS</span></span>

[<span data-ttu-id="f1a7e-128">New-AzureRmAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="f1a7e-128">New-AzureRmAnalysisServicesServer </span></span>](./New-AzureRmAnalysisServicesServer .md)

[<span data-ttu-id="f1a7e-129">Remove-AzureRmAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="f1a7e-129">Remove-AzureRmAnalysisServicesServer </span></span>](./Remove-AzureRmAnalysisServicesServer .md)
