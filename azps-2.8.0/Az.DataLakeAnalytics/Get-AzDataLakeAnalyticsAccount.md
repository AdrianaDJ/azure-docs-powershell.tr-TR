---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 4EA01047-021C-4FA5-82F0-5102BA114BC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: b0390f4ec9ec7c141e7d059c88d7aeb4b9c8507d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752407"
---
# <span data-ttu-id="432cb-101">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="432cb-101">Get-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="432cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="432cb-102">SYNOPSIS</span></span>
<span data-ttu-id="432cb-103">Data Lake Analytics hesabı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="432cb-103">Gets information about a Data Lake Analytics account.</span></span>

## <span data-ttu-id="432cb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="432cb-104">SYNTAX</span></span>

### <span data-ttu-id="432cb-105">Getallinaboneliği (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="432cb-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeAnalyticsAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="432cb-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="432cb-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="432cb-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="432cb-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeAnalyticsAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="432cb-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="432cb-108">DESCRIPTION</span></span>
<span data-ttu-id="432cb-109">**Get-Azdatalakeanalizticsaccount** cmdlet 'ı bir Azure Data Lake Analytics hesabı hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="432cb-109">The **Get-AzDataLakeAnalyticsAccount** cmdlet gets information about an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="432cb-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="432cb-110">EXAMPLES</span></span>

### <span data-ttu-id="432cb-111">Örnek 1: veri Lake Analytics hesabı hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="432cb-111">Example 1: Get information about a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="432cb-112">Bu komut, ContosoAdlAccount adlı hesap hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="432cb-112">This command gets information about the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="432cb-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="432cb-113">PARAMETERS</span></span>

### <span data-ttu-id="432cb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="432cb-114">-DefaultProfile</span></span>
<span data-ttu-id="432cb-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="432cb-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="432cb-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="432cb-116">-Name</span></span>
<span data-ttu-id="432cb-117">Data Lake Analytics hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="432cb-117">Specifies the name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="432cb-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="432cb-118">-ResourceGroupName</span></span>
<span data-ttu-id="432cb-119">Data Lake Analytics hesabının kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="432cb-119">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="432cb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="432cb-120">CommonParameters</span></span>
<span data-ttu-id="432cb-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="432cb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="432cb-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="432cb-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="432cb-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="432cb-123">INPUTS</span></span>

### <span data-ttu-id="432cb-124">System. String</span><span class="sxs-lookup"><span data-stu-id="432cb-124">System.String</span></span>

## <span data-ttu-id="432cb-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="432cb-125">OUTPUTS</span></span>

### <span data-ttu-id="432cb-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDAtalakeanaliz Ticsaccount</span><span class="sxs-lookup"><span data-stu-id="432cb-126">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

### <span data-ttu-id="432cb-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDAtalakeanaliz</span><span class="sxs-lookup"><span data-stu-id="432cb-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccountBasic</span></span>

## <span data-ttu-id="432cb-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="432cb-128">NOTES</span></span>

## <span data-ttu-id="432cb-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="432cb-129">RELATED LINKS</span></span>

[<span data-ttu-id="432cb-130">Yeni-Azdatalakeanaliz Ticsaccount</span><span class="sxs-lookup"><span data-stu-id="432cb-130">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="432cb-131">Remove-Azdatalakeanaliz Ticsaccount</span><span class="sxs-lookup"><span data-stu-id="432cb-131">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="432cb-132">Set-Azdatalakeanaliz Ticsaccount</span><span class="sxs-lookup"><span data-stu-id="432cb-132">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="432cb-133">Test-Azdatalakeanaliz Ticsaccount</span><span class="sxs-lookup"><span data-stu-id="432cb-133">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)

