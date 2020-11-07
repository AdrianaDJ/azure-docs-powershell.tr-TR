---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0B52890D-102F-4C3C-9EF9-017F6ECA3E26
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Test-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 4f3ffda3bbac6658cf54af1c7b459ce70f651e90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764863"
---
# <span data-ttu-id="f55df-101">Test-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f55df-101">Test-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="f55df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f55df-102">SYNOPSIS</span></span>
<span data-ttu-id="f55df-103">Veri Lake Analytics hesabının varlığını denetler.</span><span class="sxs-lookup"><span data-stu-id="f55df-103">Checks for the existence of a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f55df-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f55df-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f55df-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f55df-105">DESCRIPTION</span></span>
<span data-ttu-id="f55df-106">**Test-Azurermdatalakeanalizleri** , veri Lake Analytics hesabının varlığını denetler.</span><span class="sxs-lookup"><span data-stu-id="f55df-106">The **Test-AzureRmDataLakeAnalyticsAccount** cmdlet checks for the existence of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="f55df-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f55df-107">EXAMPLES</span></span>

### <span data-ttu-id="f55df-108">Örnek 1: bir hesabın bulunup bulunmadığını test etme</span><span class="sxs-lookup"><span data-stu-id="f55df-108">Example 1: Test whether an account exists</span></span>
```
PS C:\>Test-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="f55df-109">Bu komut, ContosoAdlAccount adlı hesabın var olup olmadığını sınar.</span><span class="sxs-lookup"><span data-stu-id="f55df-109">This command tests whether the account named ContosoAdlAccount exists.</span></span>

## <span data-ttu-id="f55df-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f55df-110">PARAMETERS</span></span>

### <span data-ttu-id="f55df-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="f55df-111">-Name</span></span>
<span data-ttu-id="f55df-112">Data Lake Analytics hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f55df-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="f55df-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f55df-113">-ResourceGroupName</span></span>
<span data-ttu-id="f55df-114">Data Lake Analytics hesabının kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f55df-114">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="f55df-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f55df-115">-DefaultProfile</span></span>
<span data-ttu-id="f55df-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f55df-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f55df-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f55df-117">CommonParameters</span></span>
<span data-ttu-id="f55df-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f55df-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f55df-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f55df-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f55df-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f55df-120">INPUTS</span></span>

## <span data-ttu-id="f55df-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f55df-121">OUTPUTS</span></span>

### <span data-ttu-id="f55df-122">bool</span><span class="sxs-lookup"><span data-stu-id="f55df-122">bool</span></span>
<span data-ttu-id="f55df-123">Hesabın var olup olmadığını belirten doğru veya yanlış.</span><span class="sxs-lookup"><span data-stu-id="f55df-123">True or false indicating whether the account exists or not.</span></span>

## <span data-ttu-id="f55df-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f55df-124">NOTES</span></span>

## <span data-ttu-id="f55df-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f55df-125">RELATED LINKS</span></span>

[<span data-ttu-id="f55df-126">Get-Azurermdatalakeanalyzer</span><span class="sxs-lookup"><span data-stu-id="f55df-126">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="f55df-127">Yeni-Azurermdatalakeanalyzer</span><span class="sxs-lookup"><span data-stu-id="f55df-127">New-AzureRmDataLakeAnalyticsAccount</span></span>](./New-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="f55df-128">Set-Azurermdatalakeanalyzer Ticsaccount</span><span class="sxs-lookup"><span data-stu-id="f55df-128">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)


