---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 32c7478e7e2419a8f83c839efd841f25446a96c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588503"
---
# <span data-ttu-id="0d923-101">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="0d923-101">Get-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="0d923-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d923-102">SYNOPSIS</span></span>
<span data-ttu-id="0d923-103">Data Lake Analytics hesabı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="0d923-103">Gets information about a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d923-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0d923-104">SYNTAX</span></span>

### <span data-ttu-id="0d923-105">Getallinaboneliği (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0d923-105">GetAllInSubscription (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d923-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0d923-106">GetByResourceGroup</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0d923-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="0d923-107">GetBySpecificAccount</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d923-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0d923-108">DESCRIPTION</span></span>
<span data-ttu-id="0d923-109">**Get-Azurermdatalakeanalyzer** cmdlet 'i, bir Azure Data Lake Analytics hesabı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="0d923-109">The **Get-AzureRmDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="0d923-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0d923-110">EXAMPLES</span></span>

### <span data-ttu-id="0d923-111">Örnek 1: veri Lake Analytics hesabı hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="0d923-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="0d923-112">Bu komut, ContosoAdlAccount adlı hesap hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="0d923-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="0d923-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0d923-113">PARAMETERS</span></span>

### <span data-ttu-id="0d923-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d923-114">-DefaultProfile</span></span>
<span data-ttu-id="0d923-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="0d923-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0d923-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="0d923-116">-Name</span></span>
<span data-ttu-id="0d923-117">Data Lake Analytics hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0d923-117">Specifies the name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBySpecificAccount
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d923-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d923-118">-ResourceGroupName</span></span>
<span data-ttu-id="0d923-119">Data Lake Analytics hesabının kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0d923-119">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetBySpecificAccount
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d923-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d923-120">CommonParameters</span></span>
<span data-ttu-id="0d923-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0d923-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d923-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d923-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d923-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0d923-123">INPUTS</span></span>

### <span data-ttu-id="0d923-124">System. String</span><span class="sxs-lookup"><span data-stu-id="0d923-124">System.String</span></span>

## <span data-ttu-id="0d923-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0d923-125">OUTPUTS</span></span>

### <span data-ttu-id="0d923-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDAtalakeanaliz Ticsaccount</span><span class="sxs-lookup"><span data-stu-id="0d923-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="0d923-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0d923-127">NOTES</span></span>

## <span data-ttu-id="0d923-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0d923-128">RELATED LINKS</span></span>

[<span data-ttu-id="0d923-129">Yeni-Azurermdatalakeanalyzer</span><span class="sxs-lookup"><span data-stu-id="0d923-129">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="0d923-130">Remove-Azurermdatalakeanalyzer Ticsaccount</span><span class="sxs-lookup"><span data-stu-id="0d923-130">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="0d923-131">Set-Azurermdatalakeanalyzer Ticsaccount</span><span class="sxs-lookup"><span data-stu-id="0d923-131">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="0d923-132">Test-Azurermdatalakeanalyzer</span><span class="sxs-lookup"><span data-stu-id="0d923-132">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


