---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0B52890D-102F-4C3C-9EF9-017F6ECA3E26
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/test-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: e527501424edfbbc12693b47b5858c3c46592402
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762961"
---
# <span data-ttu-id="50d60-101">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="50d60-101">Test-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="50d60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50d60-102">SYNOPSIS</span></span>
<span data-ttu-id="50d60-103">Veri Lake Analytics hesabının varlığını denetler.</span><span class="sxs-lookup"><span data-stu-id="50d60-103">Checks for the existence of a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50d60-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="50d60-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50d60-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="50d60-105">DESCRIPTION</span></span>
<span data-ttu-id="50d60-106">**Test-Azurermdatalakeanalizleri** , veri Lake Analytics hesabının varlığını denetler.</span><span class="sxs-lookup"><span data-stu-id="50d60-106">The **Test-AzureRmDataLakeAnalyticsAccount** cmdlet checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="50d60-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="50d60-107">EXAMPLES</span></span>

### <span data-ttu-id="50d60-108">Örnek 1: bir hesabın bulunup bulunmadığını test etme</span><span class="sxs-lookup"><span data-stu-id="50d60-108">Example 1: Test whether an account exists</span></span>
```
PS C:\>Test-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="50d60-109">Bu komut, ContosoAdlAccount adlı hesabın var olup olmadığını sınar.</span><span class="sxs-lookup"><span data-stu-id="50d60-109">This command tests whether the account named ContosoAdlAccount exists.</span></span>

## <span data-ttu-id="50d60-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="50d60-110">PARAMETERS</span></span>

### <span data-ttu-id="50d60-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50d60-111">-DefaultProfile</span></span>
<span data-ttu-id="50d60-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="50d60-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50d60-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="50d60-113">-Name</span></span>
<span data-ttu-id="50d60-114">Data Lake Analytics hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="50d60-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="50d60-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50d60-115">-ResourceGroupName</span></span>
<span data-ttu-id="50d60-116">Data Lake Analytics hesabının kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="50d60-116">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="50d60-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50d60-117">CommonParameters</span></span>
<span data-ttu-id="50d60-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="50d60-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50d60-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50d60-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50d60-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="50d60-120">INPUTS</span></span>

### <span data-ttu-id="50d60-121">System. String</span><span class="sxs-lookup"><span data-stu-id="50d60-121">System.String</span></span>

## <span data-ttu-id="50d60-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="50d60-122">OUTPUTS</span></span>

### <span data-ttu-id="50d60-123">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="50d60-123">System.Boolean</span></span>

## <span data-ttu-id="50d60-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="50d60-124">NOTES</span></span>

## <span data-ttu-id="50d60-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="50d60-125">RELATED LINKS</span></span>

[<span data-ttu-id="50d60-126">Get-Azurermdatalakeanalyzer</span><span class="sxs-lookup"><span data-stu-id="50d60-126">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="50d60-127">Yeni-Azurermdatalakeanalyzer</span><span class="sxs-lookup"><span data-stu-id="50d60-127">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="50d60-128">Set-Azurermdatalakeanalyzer Ticsaccount</span><span class="sxs-lookup"><span data-stu-id="50d60-128">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

