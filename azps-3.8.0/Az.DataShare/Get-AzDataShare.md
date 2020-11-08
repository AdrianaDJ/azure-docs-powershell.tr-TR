---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShare.md
ms.openlocfilehash: a01d67a5ebf98e07a9410903e4c00b4ed4ee70a2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096442"
---
# <span data-ttu-id="63f64-101">Get-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="63f64-101">Get-AzDataShare</span></span>

## <span data-ttu-id="63f64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63f64-102">SYNOPSIS</span></span>
<span data-ttu-id="63f64-103">Veri paylaşımları hakkında bilgi edinin.</span><span class="sxs-lookup"><span data-stu-id="63f64-103">Get information about Data Shares.</span></span>

## <span data-ttu-id="63f64-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="63f64-104">SYNTAX</span></span>

### <span data-ttu-id="63f64-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="63f64-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShare -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63f64-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="63f64-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63f64-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="63f64-107">DESCRIPTION</span></span>
<span data-ttu-id="63f64-108">**Get-AzDataShare** cmdlet 'i, bir Azure veri paylaşımında veri paylaşımı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="63f64-108">The **Get-AzDataShare** cmdlet gets information about data shares in an Azure data share accoount.</span></span>
<span data-ttu-id="63f64-109">Veri paylaşımının adını belirtirseniz, bu cmdlet bu veri paylaşımı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="63f64-109">If you specify the name of a data share, this cmdlet gets information about that data share.</span></span>
<span data-ttu-id="63f64-110">Bir ad belirtmezseniz, bu cmdlet bir Azure veri paylaşımı hesabındaki tüm veri paylaşımları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="63f64-110">If you do not specify a name, this cmdlet gets information about all of the data shares in an Azure data share account.</span></span>

## <span data-ttu-id="63f64-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="63f64-111">EXAMPLES</span></span>

### <span data-ttu-id="63f64-112">Örnek 1: belirli bir veri paylaşımı alma</span><span class="sxs-lookup"><span data-stu-id="63f64-112">Example 1 : Get a specific data share</span></span>
```
PS C:\>Get-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -Name "AdsShare"
Name                : AdsShare
Id                  : /subscriptions/f3ead1ff-d0ab-4cf4-9a5a-86f1661d4685/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare
Type                : Microsoft.DataShare/shares
CreatedAt           : 6/11/2019 12:00:00 AM
CreatedBy           : Contoso ADS
ShareKind           : CopyBased
Description         : Example of description  
ProvisioningState   : Succeeded
Terms               : This should not be shared
```

<span data-ttu-id="63f64-113">Bu komut, Azure veri paylaşımı hesabındaki veri paylaşımı AdsShare ile ilgili bilgileri görüntüler.</span><span class="sxs-lookup"><span data-stu-id="63f64-113">This command displays information about data share AdsShare in the Azure data share account WikiAdsAccount and resource group ADS.</span></span>

## <span data-ttu-id="63f64-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="63f64-114">PARAMETERS</span></span>

### <span data-ttu-id="63f64-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="63f64-115">-AccountName</span></span>
<span data-ttu-id="63f64-116">Azure veri paylaşımı hesap adı</span><span class="sxs-lookup"><span data-stu-id="63f64-116">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63f64-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63f64-117">-DefaultProfile</span></span>
<span data-ttu-id="63f64-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="63f64-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63f64-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="63f64-119">-Name</span></span>
<span data-ttu-id="63f64-120">Azure veri paylaşımı adı</span><span class="sxs-lookup"><span data-stu-id="63f64-120">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63f64-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63f64-121">-ResourceGroupName</span></span>
<span data-ttu-id="63f64-122">Azure veri paylaşımı hesabının kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="63f64-122">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63f64-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="63f64-123">-ResourceId</span></span>
<span data-ttu-id="63f64-124">Azure veri paylaşımı 'nın kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="63f64-124">The resource id of the azure data share</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63f64-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63f64-125">CommonParameters</span></span>
<span data-ttu-id="63f64-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="63f64-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63f64-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63f64-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63f64-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="63f64-128">INPUTS</span></span>

### <span data-ttu-id="63f64-129">System. String</span><span class="sxs-lookup"><span data-stu-id="63f64-129">System.String</span></span>

## <span data-ttu-id="63f64-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="63f64-130">OUTPUTS</span></span>

### <span data-ttu-id="63f64-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDAtapaylaşımı</span><span class="sxs-lookup"><span data-stu-id="63f64-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="63f64-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="63f64-132">NOTES</span></span>

## <span data-ttu-id="63f64-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="63f64-133">RELATED LINKS</span></span>