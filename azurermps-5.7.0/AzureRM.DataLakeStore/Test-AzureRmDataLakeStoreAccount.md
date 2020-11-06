---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 613DE097-65E0-4F08-839D-F9B53F772382
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/test-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 15c0614094ed28a9888e2e39a6cfb81547fbb6e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593508"
---
# <span data-ttu-id="b139d-101">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="b139d-101">Test-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="b139d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b139d-102">SYNOPSIS</span></span>
<span data-ttu-id="b139d-103">Veri Lake Store hesabının varlığını sınar.</span><span class="sxs-lookup"><span data-stu-id="b139d-103">Tests the existence of a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b139d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b139d-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b139d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b139d-105">DESCRIPTION</span></span>
<span data-ttu-id="b139d-106">**Test-AzureRmDataLakeStoreAccount** cmdlet 'ı Data Lake Store hesabının varlığını sınar.</span><span class="sxs-lookup"><span data-stu-id="b139d-106">The **Test-AzureRmDataLakeStoreAccount** cmdlet tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="b139d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b139d-107">EXAMPLES</span></span>

### <span data-ttu-id="b139d-108">Örnek 1: hesabı test etme</span><span class="sxs-lookup"><span data-stu-id="b139d-108">Example 1: Test an account</span></span>
```
PS C:\>Test-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="b139d-109">Bu komut, ContosoADL adlı hesabın var olup olmadığını sınar.</span><span class="sxs-lookup"><span data-stu-id="b139d-109">This command tests whether the account named ContosoADL exists.</span></span>

## <span data-ttu-id="b139d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b139d-110">PARAMETERS</span></span>

### <span data-ttu-id="b139d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b139d-111">-DefaultProfile</span></span>
<span data-ttu-id="b139d-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b139d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b139d-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="b139d-113">-Name</span></span>
<span data-ttu-id="b139d-114">Sınanacak veri Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b139d-114">Specifies the name of the Data Lake Store account to test.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b139d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b139d-115">-ResourceGroupName</span></span>
<span data-ttu-id="b139d-116">Sınanacak hesabı içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b139d-116">Specifies the name of the resource group that contains the account to test.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b139d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b139d-117">CommonParameters</span></span>
<span data-ttu-id="b139d-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b139d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b139d-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b139d-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b139d-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b139d-120">INPUTS</span></span>

### <span data-ttu-id="b139d-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b139d-121">None</span></span>
<span data-ttu-id="b139d-122">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="b139d-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b139d-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b139d-123">OUTPUTS</span></span>

### <span data-ttu-id="b139d-124">bool</span><span class="sxs-lookup"><span data-stu-id="b139d-124">bool</span></span>
<span data-ttu-id="b139d-125">Belirtilen hesabın varlığını belirten doğru veya yanlış.</span><span class="sxs-lookup"><span data-stu-id="b139d-125">True or false indicating the existence of the specified account.</span></span>

## <span data-ttu-id="b139d-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b139d-126">NOTES</span></span>

## <span data-ttu-id="b139d-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b139d-127">RELATED LINKS</span></span>

[<span data-ttu-id="b139d-128">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="b139d-128">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="b139d-129">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="b139d-129">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="b139d-130">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="b139d-130">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="b139d-131">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="b139d-131">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)


