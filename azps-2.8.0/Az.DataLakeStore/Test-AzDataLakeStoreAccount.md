---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 613DE097-65E0-4F08-839D-F9B53F772382
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/test-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreAccount.md
ms.openlocfilehash: 887dca3fa7a2155b07cd570a92a94a25e4346541
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752268"
---
# <span data-ttu-id="56b81-101">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="56b81-101">Test-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="56b81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56b81-102">SYNOPSIS</span></span>
<span data-ttu-id="56b81-103">Veri Lake Store hesabının varlığını sınar.</span><span class="sxs-lookup"><span data-stu-id="56b81-103">Tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="56b81-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="56b81-104">SYNTAX</span></span>

```
Test-AzDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56b81-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="56b81-105">DESCRIPTION</span></span>
<span data-ttu-id="56b81-106">**Test-AzDataLakeStoreAccount** cmdlet 'ı Data Lake Store hesabının varlığını sınar.</span><span class="sxs-lookup"><span data-stu-id="56b81-106">The **Test-AzDataLakeStoreAccount** cmdlet tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="56b81-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="56b81-107">EXAMPLES</span></span>

### <span data-ttu-id="56b81-108">Örnek 1: hesabı test etme</span><span class="sxs-lookup"><span data-stu-id="56b81-108">Example 1: Test an account</span></span>
```
PS C:\>Test-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="56b81-109">Bu komut, ContosoADL adlı hesabın var olup olmadığını sınar.</span><span class="sxs-lookup"><span data-stu-id="56b81-109">This command tests whether the account named ContosoADL exists.</span></span>

## <span data-ttu-id="56b81-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="56b81-110">PARAMETERS</span></span>

### <span data-ttu-id="56b81-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56b81-111">-DefaultProfile</span></span>
<span data-ttu-id="56b81-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="56b81-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="56b81-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="56b81-113">-Name</span></span>
<span data-ttu-id="56b81-114">Sınanacak veri Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="56b81-114">Specifies the name of the Data Lake Store account to test.</span></span>

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

### <span data-ttu-id="56b81-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56b81-115">-ResourceGroupName</span></span>
<span data-ttu-id="56b81-116">Sınanacak hesabı içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="56b81-116">Specifies the name of the resource group that contains the account to test.</span></span>

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

### <span data-ttu-id="56b81-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56b81-117">CommonParameters</span></span>
<span data-ttu-id="56b81-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="56b81-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56b81-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56b81-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56b81-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="56b81-120">INPUTS</span></span>

### <span data-ttu-id="56b81-121">System. String</span><span class="sxs-lookup"><span data-stu-id="56b81-121">System.String</span></span>

## <span data-ttu-id="56b81-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="56b81-122">OUTPUTS</span></span>

### <span data-ttu-id="56b81-123">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="56b81-123">System.Boolean</span></span>

## <span data-ttu-id="56b81-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="56b81-124">NOTES</span></span>

## <span data-ttu-id="56b81-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="56b81-125">RELATED LINKS</span></span>

[<span data-ttu-id="56b81-126">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="56b81-126">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="56b81-127">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="56b81-127">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="56b81-128">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="56b81-128">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="56b81-129">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="56b81-129">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)


