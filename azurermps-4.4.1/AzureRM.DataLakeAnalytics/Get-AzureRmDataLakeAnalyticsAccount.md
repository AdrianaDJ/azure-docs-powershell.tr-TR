---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 1ab8cbd8ead120ecc531e3e252fe2c31a58f10c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762224"
---
# <span data-ttu-id="bf09c-101">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="bf09c-101">Get-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="bf09c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf09c-102">SYNOPSIS</span></span>
<span data-ttu-id="bf09c-103">Data Lake Analytics hesabı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="bf09c-103">Gets information about a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf09c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bf09c-104">SYNTAX</span></span>

### <span data-ttu-id="bf09c-105">Tüm abonelikte (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bf09c-105">All In Subscription (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf09c-106">Tümü kaynak grubunda</span><span class="sxs-lookup"><span data-stu-id="bf09c-106">All In Resource Group</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bf09c-107">Belirli bir hesap</span><span class="sxs-lookup"><span data-stu-id="bf09c-107">Specific Account</span></span>
```
Get-AzureRmDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf09c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="bf09c-108">DESCRIPTION</span></span>
<span data-ttu-id="bf09c-109">**Get-Azurermdatalakeanalyzer** cmdlet 'i, bir Azure Data Lake Analytics hesabı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="bf09c-109">The **Get-AzureRmDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="bf09c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bf09c-110">EXAMPLES</span></span>

### <span data-ttu-id="bf09c-111">Örnek 1: veri Lake Analytics hesabı hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="bf09c-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="bf09c-112">Bu komut, ContosoAdlAccount adlı hesap hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="bf09c-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="bf09c-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bf09c-113">PARAMETERS</span></span>

### <span data-ttu-id="bf09c-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="bf09c-114">-Name</span></span>
<span data-ttu-id="bf09c-115">Data Lake Analytics hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf09c-115">Specifies the name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific Account
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf09c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf09c-116">-ResourceGroupName</span></span>
<span data-ttu-id="bf09c-117">Data Lake Analytics hesabının kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf09c-117">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: All In Resource Group
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Specific Account
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf09c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf09c-118">-DefaultProfile</span></span>
<span data-ttu-id="bf09c-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bf09c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf09c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf09c-120">CommonParameters</span></span>
<span data-ttu-id="bf09c-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bf09c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf09c-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf09c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf09c-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bf09c-123">INPUTS</span></span>

## <span data-ttu-id="bf09c-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bf09c-124">OUTPUTS</span></span>

### <span data-ttu-id="bf09c-125">Psdatalakeanalyzer Ticsaccount</span><span class="sxs-lookup"><span data-stu-id="bf09c-125">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="bf09c-126">Belirtilen hesap ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="bf09c-126">The specified account details.</span></span>

### <span data-ttu-id="bf09c-127">Listeniz<PSDataLakeAnalyticsAccount></span><span class="sxs-lookup"><span data-stu-id="bf09c-127">List<PSDataLakeAnalyticsAccount></span></span>
<span data-ttu-id="bf09c-128">Belirtilen kaynak grubundaki veya abonelikteki hesap listesi.</span><span class="sxs-lookup"><span data-stu-id="bf09c-128">The list of accounts in the specified resource group or subscription.</span></span>

## <span data-ttu-id="bf09c-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bf09c-129">NOTES</span></span>

## <span data-ttu-id="bf09c-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bf09c-130">RELATED LINKS</span></span>

[<span data-ttu-id="bf09c-131">Yeni-Azurermdatalakeanalyzer</span><span class="sxs-lookup"><span data-stu-id="bf09c-131">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="bf09c-132">Remove-Azurermdatalakeanalyzer Ticsaccount</span><span class="sxs-lookup"><span data-stu-id="bf09c-132">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="bf09c-133">Set-Azurermdatalakeanalyzer Ticsaccount</span><span class="sxs-lookup"><span data-stu-id="bf09c-133">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="bf09c-134">Test-Azurermdatalakeanalyzer</span><span class="sxs-lookup"><span data-stu-id="bf09c-134">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


