---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: f15ef7201622394a2b96964244980b059f1222c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572821"
---
# <span data-ttu-id="92547-101">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="92547-101">Get-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="92547-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92547-102">SYNOPSIS</span></span>
<span data-ttu-id="92547-103">Data Lake Store hesabının ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="92547-103">Gets details of a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92547-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="92547-104">SYNTAX</span></span>

### <span data-ttu-id="92547-105">Getallinaboneliği (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="92547-105">GetAllInSubscription (Default)</span></span>
```
Get-AzureRmDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92547-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="92547-106">GetByResourceGroup</span></span>
```
Get-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="92547-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="92547-107">GetBySpecificAccount</span></span>
```
Get-AzureRmDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92547-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="92547-108">DESCRIPTION</span></span>
<span data-ttu-id="92547-109">**Get-AzureRmDataLakeStoreAccount** cmdlet 'ı Data Lake Store hesabının ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="92547-109">The **Get-AzureRmDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="92547-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="92547-110">EXAMPLES</span></span>

### <span data-ttu-id="92547-111">Örnek 1: Data Lake Store hesabını edinme</span><span class="sxs-lookup"><span data-stu-id="92547-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="92547-112">Bu komut, ContosoADL adlı hesabı alır.</span><span class="sxs-lookup"><span data-stu-id="92547-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="92547-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="92547-113">PARAMETERS</span></span>

### <span data-ttu-id="92547-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92547-114">-DefaultProfile</span></span>
<span data-ttu-id="92547-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="92547-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="92547-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="92547-116">-Name</span></span>
<span data-ttu-id="92547-117">Alınacak hesabın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="92547-117">Specifies the name of the account to get.</span></span>

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

### <span data-ttu-id="92547-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92547-118">-ResourceGroupName</span></span>
<span data-ttu-id="92547-119">Alınacak veri Lake Store hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="92547-119">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

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

### <span data-ttu-id="92547-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92547-120">CommonParameters</span></span>
<span data-ttu-id="92547-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="92547-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92547-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92547-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92547-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="92547-123">INPUTS</span></span>

### <span data-ttu-id="92547-124">System. String</span><span class="sxs-lookup"><span data-stu-id="92547-124">System.String</span></span>

## <span data-ttu-id="92547-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="92547-125">OUTPUTS</span></span>

### <span data-ttu-id="92547-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="92547-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="92547-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="92547-127">NOTES</span></span>

## <span data-ttu-id="92547-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="92547-128">RELATED LINKS</span></span>

[<span data-ttu-id="92547-129">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="92547-129">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="92547-130">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="92547-130">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="92547-131">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="92547-131">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="92547-132">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="92547-132">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


