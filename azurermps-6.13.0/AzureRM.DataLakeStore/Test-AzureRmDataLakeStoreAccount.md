---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 613DE097-65E0-4F08-839D-F9B53F772382
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/test-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: b1b3a05b6f2d19ba350567c8793822d4129c5445
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93761972"
---
# <span data-ttu-id="5c28a-101">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5c28a-101">Test-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="5c28a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c28a-102">SYNOPSIS</span></span>
<span data-ttu-id="5c28a-103">Veri Lake Store hesabının varlığını sınar.</span><span class="sxs-lookup"><span data-stu-id="5c28a-103">Tests the existence of a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c28a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5c28a-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c28a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5c28a-105">DESCRIPTION</span></span>
<span data-ttu-id="5c28a-106">**Test-AzureRmDataLakeStoreAccount** cmdlet 'ı Data Lake Store hesabının varlığını sınar.</span><span class="sxs-lookup"><span data-stu-id="5c28a-106">The **Test-AzureRmDataLakeStoreAccount** cmdlet tests the existence of a Data Lake Store account.</span></span>

## <span data-ttu-id="5c28a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5c28a-107">EXAMPLES</span></span>

### <span data-ttu-id="5c28a-108">Örnek 1: hesabı test etme</span><span class="sxs-lookup"><span data-stu-id="5c28a-108">Example 1: Test an account</span></span>
```
PS C:\>Test-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="5c28a-109">Bu komut, ContosoADL adlı hesabın var olup olmadığını sınar.</span><span class="sxs-lookup"><span data-stu-id="5c28a-109">This command tests whether the account named ContosoADL exists.</span></span>

## <span data-ttu-id="5c28a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5c28a-110">PARAMETERS</span></span>

### <span data-ttu-id="5c28a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c28a-111">-DefaultProfile</span></span>
<span data-ttu-id="5c28a-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5c28a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c28a-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="5c28a-113">-Name</span></span>
<span data-ttu-id="5c28a-114">Sınanacak veri Lake Store hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c28a-114">Specifies the name of the Data Lake Store account to test.</span></span>

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

### <span data-ttu-id="5c28a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c28a-115">-ResourceGroupName</span></span>
<span data-ttu-id="5c28a-116">Sınanacak hesabı içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c28a-116">Specifies the name of the resource group that contains the account to test.</span></span>

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

### <span data-ttu-id="5c28a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c28a-117">CommonParameters</span></span>
<span data-ttu-id="5c28a-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5c28a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c28a-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c28a-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c28a-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5c28a-120">INPUTS</span></span>

### <span data-ttu-id="5c28a-121">System. String</span><span class="sxs-lookup"><span data-stu-id="5c28a-121">System.String</span></span>

## <span data-ttu-id="5c28a-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5c28a-122">OUTPUTS</span></span>

### <span data-ttu-id="5c28a-123">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5c28a-123">System.Boolean</span></span>

## <span data-ttu-id="5c28a-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5c28a-124">NOTES</span></span>

## <span data-ttu-id="5c28a-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5c28a-125">RELATED LINKS</span></span>

[<span data-ttu-id="5c28a-126">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5c28a-126">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="5c28a-127">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5c28a-127">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="5c28a-128">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5c28a-128">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="5c28a-129">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="5c28a-129">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)


