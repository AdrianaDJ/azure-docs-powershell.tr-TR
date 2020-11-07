---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/test-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
ms.openlocfilehash: 7298612cf64b4f90f65ebaa2943b38102b5ae1ff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753626"
---
# <span data-ttu-id="633f2-101">Test-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="633f2-101">Test-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="633f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="633f2-102">SYNOPSIS</span></span>
<span data-ttu-id="633f2-103">Analysis Services sunucusu örneğinin varlığını sınar</span><span class="sxs-lookup"><span data-stu-id="633f2-103">Tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="633f2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="633f2-104">SYNTAX</span></span>

```
Test-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="633f2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="633f2-105">DESCRIPTION</span></span>
<span data-ttu-id="633f2-106">Test-AzAnalysisServicesServer cmdlet 'i Analysis Services sunucusu örneğinin varlığını sınar</span><span class="sxs-lookup"><span data-stu-id="633f2-106">The Test-AzAnalysisServicesServer cmdlet tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="633f2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="633f2-107">EXAMPLES</span></span>

### <span data-ttu-id="633f2-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="633f2-108">Example 1</span></span>
```
PS C:\> Test-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="633f2-109">Resourcegroup testgroup 'ta TestServer adlı bir sunucu varsa bu komut test edecektir</span><span class="sxs-lookup"><span data-stu-id="633f2-109">This command will test if there is a server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="633f2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="633f2-110">PARAMETERS</span></span>

### <span data-ttu-id="633f2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="633f2-111">-DefaultProfile</span></span>
<span data-ttu-id="633f2-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="633f2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="633f2-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="633f2-113">-Name</span></span>
<span data-ttu-id="633f2-114">Analysis Services sunucusunun adı</span><span class="sxs-lookup"><span data-stu-id="633f2-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="633f2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="633f2-115">-ResourceGroupName</span></span>
<span data-ttu-id="633f2-116">Sunucunun ait olduğu Azure Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="633f2-116">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="633f2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="633f2-117">CommonParameters</span></span>
<span data-ttu-id="633f2-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="633f2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="633f2-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="633f2-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="633f2-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="633f2-120">INPUTS</span></span>

### <span data-ttu-id="633f2-121">System. String</span><span class="sxs-lookup"><span data-stu-id="633f2-121">System.String</span></span>

## <span data-ttu-id="633f2-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="633f2-122">OUTPUTS</span></span>

### <span data-ttu-id="633f2-123">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="633f2-123">System.Boolean</span></span>

## <span data-ttu-id="633f2-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="633f2-124">NOTES</span></span>
<span data-ttu-id="633f2-125">Diğer ad: Test-AzAs</span><span class="sxs-lookup"><span data-stu-id="633f2-125">Alias: Test-AzAs</span></span>

## <span data-ttu-id="633f2-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="633f2-126">RELATED LINKS</span></span>

[<span data-ttu-id="633f2-127">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="633f2-127">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="633f2-128">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="633f2-128">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
