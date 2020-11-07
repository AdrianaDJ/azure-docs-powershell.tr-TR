---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0B52890D-102F-4C3C-9EF9-017F6ECA3E26
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/test-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Test-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 77247853fe6412b0d01fb01c71e592efca12063d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916927"
---
# <span data-ttu-id="d4342-101">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="d4342-101">Test-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="d4342-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4342-102">SYNOPSIS</span></span>
<span data-ttu-id="d4342-103">Veri Lake Analytics hesabının varlığını denetler.</span><span class="sxs-lookup"><span data-stu-id="d4342-103">Checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="d4342-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d4342-104">SYNTAX</span></span>

```
Test-AzDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4342-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d4342-105">DESCRIPTION</span></span>
<span data-ttu-id="d4342-106">**Test-Azverilakeanalizleri Ticsaccount** cmdlet 'ı, veri Lake Analytics hesabının varlığını denetler.</span><span class="sxs-lookup"><span data-stu-id="d4342-106">The **Test-AzDataLakeAnalyticsAccount** cmdlet checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="d4342-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d4342-107">EXAMPLES</span></span>

### <span data-ttu-id="d4342-108">Örnek 1: bir hesabın bulunup bulunmadığını test etme</span><span class="sxs-lookup"><span data-stu-id="d4342-108">Example 1: Test whether an account exists</span></span>
```
PS C:\>Test-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="d4342-109">Bu komut, ContosoAdlAccount adlı hesabın var olup olmadığını sınar.</span><span class="sxs-lookup"><span data-stu-id="d4342-109">This command tests whether the account named ContosoAdlAccount exists.</span></span>

## <span data-ttu-id="d4342-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d4342-110">PARAMETERS</span></span>

### <span data-ttu-id="d4342-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4342-111">-DefaultProfile</span></span>
<span data-ttu-id="d4342-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d4342-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4342-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="d4342-113">-Name</span></span>
<span data-ttu-id="d4342-114">Data Lake Analytics hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4342-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="d4342-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4342-115">-ResourceGroupName</span></span>
<span data-ttu-id="d4342-116">Data Lake Analytics hesabının kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4342-116">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="d4342-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4342-117">CommonParameters</span></span>
<span data-ttu-id="d4342-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d4342-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4342-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4342-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4342-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d4342-120">INPUTS</span></span>

### <span data-ttu-id="d4342-121">System. String</span><span class="sxs-lookup"><span data-stu-id="d4342-121">System.String</span></span>

## <span data-ttu-id="d4342-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d4342-122">OUTPUTS</span></span>

### <span data-ttu-id="d4342-123">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d4342-123">System.Boolean</span></span>

## <span data-ttu-id="d4342-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d4342-124">NOTES</span></span>

## <span data-ttu-id="d4342-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d4342-125">RELATED LINKS</span></span>

[<span data-ttu-id="d4342-126">Get-Azdatalakeanaliz Ticsaccount</span><span class="sxs-lookup"><span data-stu-id="d4342-126">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="d4342-127">Yeni-Azdatalakeanaliz Ticsaccount</span><span class="sxs-lookup"><span data-stu-id="d4342-127">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="d4342-128">Set-Azdatalakeanaliz Ticsaccount</span><span class="sxs-lookup"><span data-stu-id="d4342-128">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)


