---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/test-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
ms.openlocfilehash: 86a82d5c82cdb775e7b07c6189244e494d14c4a8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109267"
---
# <span data-ttu-id="25b2e-101">Test-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="25b2e-101">Test-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="25b2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25b2e-102">SYNOPSIS</span></span>
<span data-ttu-id="25b2e-103">Analysis Services sunucusu örneğinin varlığını sınar</span><span class="sxs-lookup"><span data-stu-id="25b2e-103">Tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="25b2e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="25b2e-104">SYNTAX</span></span>

```
Test-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25b2e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="25b2e-105">DESCRIPTION</span></span>
<span data-ttu-id="25b2e-106">Test-AzAnalysisServicesServer cmdlet 'i Analysis Services sunucusu örneğinin varlığını sınar</span><span class="sxs-lookup"><span data-stu-id="25b2e-106">The Test-AzAnalysisServicesServer cmdlet tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="25b2e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="25b2e-107">EXAMPLES</span></span>

### <span data-ttu-id="25b2e-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="25b2e-108">Example 1</span></span>
```
PS C:\> Test-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="25b2e-109">Resourcegroup testgroup 'ta TestServer adlı bir sunucu varsa bu komut test edecektir</span><span class="sxs-lookup"><span data-stu-id="25b2e-109">This command will test if there is a server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="25b2e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="25b2e-110">PARAMETERS</span></span>

### <span data-ttu-id="25b2e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25b2e-111">-DefaultProfile</span></span>
<span data-ttu-id="25b2e-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="25b2e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25b2e-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="25b2e-113">-Name</span></span>
<span data-ttu-id="25b2e-114">Analysis Services sunucusunun adı</span><span class="sxs-lookup"><span data-stu-id="25b2e-114">Name of the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25b2e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25b2e-115">-ResourceGroupName</span></span>
<span data-ttu-id="25b2e-116">Sunucunun ait olduğu Azure Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="25b2e-116">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="25b2e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25b2e-117">CommonParameters</span></span>
<span data-ttu-id="25b2e-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="25b2e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25b2e-119">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25b2e-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25b2e-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="25b2e-120">INPUTS</span></span>

### <span data-ttu-id="25b2e-121">System. String</span><span class="sxs-lookup"><span data-stu-id="25b2e-121">System.String</span></span>

## <span data-ttu-id="25b2e-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="25b2e-122">OUTPUTS</span></span>

### <span data-ttu-id="25b2e-123">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="25b2e-123">System.Boolean</span></span>

## <span data-ttu-id="25b2e-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="25b2e-124">NOTES</span></span>
<span data-ttu-id="25b2e-125">Diğer ad: Test-AzAs</span><span class="sxs-lookup"><span data-stu-id="25b2e-125">Alias: Test-AzAs</span></span>

## <span data-ttu-id="25b2e-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="25b2e-126">RELATED LINKS</span></span>

[<span data-ttu-id="25b2e-127">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="25b2e-127">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="25b2e-128">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="25b2e-128">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
