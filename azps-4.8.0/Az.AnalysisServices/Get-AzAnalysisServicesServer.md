---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/get-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Get-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Get-AzAnalysisServicesServer.md
ms.openlocfilehash: c0c308bfe9d2d5fad971f9df1a26b03710d5629c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268155"
---
# <span data-ttu-id="b3cdb-101">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="b3cdb-101">Get-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="b3cdb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3cdb-102">SYNOPSIS</span></span>
<span data-ttu-id="b3cdb-103">Analysis Services sunucusunun ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="b3cdb-103">Gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="b3cdb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b3cdb-104">SYNTAX</span></span>

```
Get-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3cdb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b3cdb-105">DESCRIPTION</span></span>
<span data-ttu-id="b3cdb-106">Get-AzAnalysisServicesServer cmdlet 'i Analysis Services sunucusunun ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="b3cdb-106">The Get-AzAnalysisServicesServer cmdlet gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="b3cdb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b3cdb-107">EXAMPLES</span></span>

### <span data-ttu-id="b3cdb-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b3cdb-108">Example 1</span></span>
```
PS C:\>Get-AzAnalysisServicesServer -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="b3cdb-109">Bu komut, ResourceGroup03 adındaki kaynak grubundaki tüm Azure Analysis Services sunucularını alır.</span><span class="sxs-lookup"><span data-stu-id="b3cdb-109">This command gets all Azure Analysis Services servers in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="b3cdb-110">Örnek 2: sunucu edinme</span><span class="sxs-lookup"><span data-stu-id="b3cdb-110">Example 2: Get a server</span></span>
```
PS C:\>Get-AzAnalysisServicesServer -ResourceGroupName "ResourceGroup03" -Name "testserver"
```

<span data-ttu-id="b3cdb-111">Bu komut, ResourceGroup03 adlı kaynak grubunda TestServer adlı Azure Analysis Services sunucusunu alır.</span><span class="sxs-lookup"><span data-stu-id="b3cdb-111">This command gets the Azure Analysis Services server named testserver in the resource group named ResourceGroup03.</span></span>

## <span data-ttu-id="b3cdb-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b3cdb-112">PARAMETERS</span></span>

### <span data-ttu-id="b3cdb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3cdb-113">-DefaultProfile</span></span>
<span data-ttu-id="b3cdb-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b3cdb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3cdb-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="b3cdb-115">-Name</span></span>
<span data-ttu-id="b3cdb-116">Analysis Services sunucusunun adı</span><span class="sxs-lookup"><span data-stu-id="b3cdb-116">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="b3cdb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3cdb-117">-ResourceGroupName</span></span>
<span data-ttu-id="b3cdb-118">Sunucunun ait olduğu Azure Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="b3cdb-118">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="b3cdb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3cdb-119">CommonParameters</span></span>
<span data-ttu-id="b3cdb-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b3cdb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3cdb-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3cdb-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3cdb-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b3cdb-122">INPUTS</span></span>

### <span data-ttu-id="b3cdb-123">System. String</span><span class="sxs-lookup"><span data-stu-id="b3cdb-123">System.String</span></span>

## <span data-ttu-id="b3cdb-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b3cdb-124">OUTPUTS</span></span>

### <span data-ttu-id="b3cdb-125">Microsoft. Azure. Commands. AnalysisServices. modeller. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="b3cdb-125">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="b3cdb-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b3cdb-126">NOTES</span></span>
<span data-ttu-id="b3cdb-127">Diğer ad: Get-AzAs</span><span class="sxs-lookup"><span data-stu-id="b3cdb-127">Alias: Get-AzAs</span></span>

## <span data-ttu-id="b3cdb-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b3cdb-128">RELATED LINKS</span></span>

[<span data-ttu-id="b3cdb-129">Yeni-AzAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="b3cdb-129">New-AzAnalysisServicesServer </span></span>](./New-AzAnalysisServicesServer .md)

[<span data-ttu-id="b3cdb-130">Remove-AzAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="b3cdb-130">Remove-AzAnalysisServicesServer </span></span>](./Remove-AzAnalysisServicesServer .md)
