---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 71d524aeea441c80b90642a01f1a2f34996904ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762380"
---
# <span data-ttu-id="49a9f-101">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="49a9f-101">Get-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="49a9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49a9f-102">SYNOPSIS</span></span>
<span data-ttu-id="49a9f-103">Data Lake Analytics hesabı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="49a9f-103">Gets information about a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49a9f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="49a9f-104">SYNTAX</span></span>

### <span data-ttu-id="49a9f-105">Getallinaboneliği (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="49a9f-105">GetAllInSubscription (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49a9f-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="49a9f-106">GetByResourceGroup</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="49a9f-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="49a9f-107">GetBySpecificAccount</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49a9f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="49a9f-108">DESCRIPTION</span></span>
<span data-ttu-id="49a9f-109">**Get-Azurermdatalakeanalyzer** cmdlet 'i, bir Azure Data Lake Analytics hesabı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="49a9f-109">The **Get-AzureRmDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="49a9f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="49a9f-110">EXAMPLES</span></span>

### <span data-ttu-id="49a9f-111">Örnek 1: veri Lake Analytics hesabı hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="49a9f-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="49a9f-112">Bu komut, ContosoAdlAccount adlı hesap hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="49a9f-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="49a9f-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="49a9f-113">PARAMETERS</span></span>

### <span data-ttu-id="49a9f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49a9f-114">-DefaultProfile</span></span>
<span data-ttu-id="49a9f-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="49a9f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49a9f-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="49a9f-116">-Name</span></span>
<span data-ttu-id="49a9f-117">Data Lake Analytics hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="49a9f-117">Specifies the name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecificAccount
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49a9f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49a9f-118">-ResourceGroupName</span></span>
<span data-ttu-id="49a9f-119">Data Lake Analytics hesabının kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="49a9f-119">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetBySpecificAccount
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49a9f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49a9f-120">CommonParameters</span></span>
<span data-ttu-id="49a9f-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="49a9f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49a9f-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49a9f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49a9f-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="49a9f-123">INPUTS</span></span>

### <span data-ttu-id="49a9f-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="49a9f-124">None</span></span>
<span data-ttu-id="49a9f-125">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="49a9f-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="49a9f-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="49a9f-126">OUTPUTS</span></span>

### <span data-ttu-id="49a9f-127">Psdatalakeanalyzer Ticsaccount</span><span class="sxs-lookup"><span data-stu-id="49a9f-127">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="49a9f-128">Belirtilen hesap ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="49a9f-128">The specified account details.</span></span>

### <span data-ttu-id="49a9f-129">Listeniz<PSDataLakeAnalyticsAccountBasic></span><span class="sxs-lookup"><span data-stu-id="49a9f-129">List<PSDataLakeAnalyticsAccountBasic></span></span>
<span data-ttu-id="49a9f-130">Belirtilen kaynak grubundaki veya abonelikteki hesap listesi.</span><span class="sxs-lookup"><span data-stu-id="49a9f-130">The list of accounts in the specified resource group or subscription.</span></span>

## <span data-ttu-id="49a9f-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="49a9f-131">NOTES</span></span>

## <span data-ttu-id="49a9f-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="49a9f-132">RELATED LINKS</span></span>

[<span data-ttu-id="49a9f-133">Yeni-Azurermdatalakeanalyzer</span><span class="sxs-lookup"><span data-stu-id="49a9f-133">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="49a9f-134">Remove-Azurermdatalakeanalyzer Ticsaccount</span><span class="sxs-lookup"><span data-stu-id="49a9f-134">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="49a9f-135">Set-Azurermdatalakeanalyzer Ticsaccount</span><span class="sxs-lookup"><span data-stu-id="49a9f-135">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="49a9f-136">Test-Azurermdatalakeanalyzer</span><span class="sxs-lookup"><span data-stu-id="49a9f-136">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


