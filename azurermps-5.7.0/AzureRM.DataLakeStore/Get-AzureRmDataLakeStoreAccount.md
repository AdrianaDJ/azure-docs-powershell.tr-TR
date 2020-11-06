---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 61899a50c857fc3e8852d362d5905b0ca2fedf6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591693"
---
# <span data-ttu-id="dbee7-101">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="dbee7-101">Get-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="dbee7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbee7-102">SYNOPSIS</span></span>
<span data-ttu-id="dbee7-103">Data Lake Store hesabının ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="dbee7-103">Gets details of a Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dbee7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dbee7-104">SYNTAX</span></span>

### <span data-ttu-id="dbee7-105">Getallinaboneliği (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dbee7-105">GetAllInSubscription (Default)</span></span>
```
Get-AzureRmDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbee7-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="dbee7-106">GetByResourceGroup</span></span>
```
Get-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dbee7-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="dbee7-107">GetBySpecificAccount</span></span>
```
Get-AzureRmDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbee7-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="dbee7-108">DESCRIPTION</span></span>
<span data-ttu-id="dbee7-109">**Get-AzureRmDataLakeStoreAccount** cmdlet 'ı Data Lake Store hesabının ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="dbee7-109">The **Get-AzureRmDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="dbee7-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dbee7-110">EXAMPLES</span></span>

### <span data-ttu-id="dbee7-111">Örnek 1: Data Lake Store hesabını edinme</span><span class="sxs-lookup"><span data-stu-id="dbee7-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="dbee7-112">Bu komut, ContosoADL adlı hesabı alır.</span><span class="sxs-lookup"><span data-stu-id="dbee7-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="dbee7-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dbee7-113">PARAMETERS</span></span>

### <span data-ttu-id="dbee7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbee7-114">-DefaultProfile</span></span>
<span data-ttu-id="dbee7-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="dbee7-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dbee7-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="dbee7-116">-Name</span></span>
<span data-ttu-id="dbee7-117">Alınacak hesabın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dbee7-117">Specifies the name of the account to get.</span></span>

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

### <span data-ttu-id="dbee7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbee7-118">-ResourceGroupName</span></span>
<span data-ttu-id="dbee7-119">Alınacak veri Lake Store hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dbee7-119">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

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

### <span data-ttu-id="dbee7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbee7-120">CommonParameters</span></span>
<span data-ttu-id="dbee7-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dbee7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbee7-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbee7-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbee7-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dbee7-123">INPUTS</span></span>

### <span data-ttu-id="dbee7-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="dbee7-124">None</span></span>
<span data-ttu-id="dbee7-125">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="dbee7-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dbee7-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dbee7-126">OUTPUTS</span></span>

### <span data-ttu-id="dbee7-127">PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="dbee7-127">PSDataLakeStoreAccount</span></span>
<span data-ttu-id="dbee7-128">Özel veri Lake Store hesabı sorulur.</span><span class="sxs-lookup"><span data-stu-id="dbee7-128">The specific Data Lake Store account asked for.</span></span>

### <span data-ttu-id="dbee7-129">Listeniz<PSDataLakeStoreAccountBasic></span><span class="sxs-lookup"><span data-stu-id="dbee7-129">List<PSDataLakeStoreAccountBasic></span></span>
<span data-ttu-id="dbee7-130">Belirtilen kaynak grubundaki veya abonelikteki veri Lake Store hesaplarının listesi.</span><span class="sxs-lookup"><span data-stu-id="dbee7-130">A list of Data Lake Store accounts in the resource group or subscription specified.</span></span>

## <span data-ttu-id="dbee7-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dbee7-131">NOTES</span></span>

## <span data-ttu-id="dbee7-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dbee7-132">RELATED LINKS</span></span>

[<span data-ttu-id="dbee7-133">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="dbee7-133">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="dbee7-134">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="dbee7-134">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="dbee7-135">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="dbee7-135">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="dbee7-136">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="dbee7-136">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


