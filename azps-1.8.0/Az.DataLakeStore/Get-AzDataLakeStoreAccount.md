---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 234D579E-B62D-4D70-8D2E-22AC0D9AC513
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreAccount.md
ms.openlocfilehash: b06b64b81679d1f0f9429be0362f936046e54ee5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916904"
---
# <span data-ttu-id="47b91-101">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="47b91-101">Get-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="47b91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47b91-102">SYNOPSIS</span></span>
<span data-ttu-id="47b91-103">Data Lake Store hesabının ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="47b91-103">Gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="47b91-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="47b91-104">SYNTAX</span></span>

### <span data-ttu-id="47b91-105">Getallinaboneliği (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="47b91-105">GetAllInSubscription (Default)</span></span>
```
Get-AzDataLakeStoreAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47b91-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="47b91-106">GetByResourceGroup</span></span>
```
Get-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="47b91-107">GetBySpecificAccount</span><span class="sxs-lookup"><span data-stu-id="47b91-107">GetBySpecificAccount</span></span>
```
Get-AzDataLakeStoreAccount [[-ResourceGroupName] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47b91-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="47b91-108">DESCRIPTION</span></span>
<span data-ttu-id="47b91-109">**Get-AzDataLakeStoreAccount** cmdlet 'ı Data Lake Store hesabının ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="47b91-109">The **Get-AzDataLakeStoreAccount** cmdlet gets details of a Data Lake Store account.</span></span>

## <span data-ttu-id="47b91-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="47b91-110">EXAMPLES</span></span>

### <span data-ttu-id="47b91-111">Örnek 1: Data Lake Store hesabını edinme</span><span class="sxs-lookup"><span data-stu-id="47b91-111">Example 1: Get a Data Lake Store account</span></span>
```
PS C:\>Get-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="47b91-112">Bu komut, ContosoADL adlı hesabı alır.</span><span class="sxs-lookup"><span data-stu-id="47b91-112">This command gets the account named ContosoADL.</span></span>

## <span data-ttu-id="47b91-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="47b91-113">PARAMETERS</span></span>

### <span data-ttu-id="47b91-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47b91-114">-DefaultProfile</span></span>
<span data-ttu-id="47b91-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="47b91-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="47b91-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="47b91-116">-Name</span></span>
<span data-ttu-id="47b91-117">Alınacak hesabın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="47b91-117">Specifies the name of the account to get.</span></span>

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

### <span data-ttu-id="47b91-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47b91-118">-ResourceGroupName</span></span>
<span data-ttu-id="47b91-119">Alınacak veri Lake Store hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="47b91-119">Specifies the name of the resource group that contains the Data Lake Store account to get.</span></span>

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

### <span data-ttu-id="47b91-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47b91-120">CommonParameters</span></span>
<span data-ttu-id="47b91-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="47b91-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47b91-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47b91-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47b91-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="47b91-123">INPUTS</span></span>

### <span data-ttu-id="47b91-124">System. String</span><span class="sxs-lookup"><span data-stu-id="47b91-124">System.String</span></span>

## <span data-ttu-id="47b91-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="47b91-125">OUTPUTS</span></span>

### <span data-ttu-id="47b91-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="47b91-126">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="47b91-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="47b91-127">NOTES</span></span>

## <span data-ttu-id="47b91-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="47b91-128">RELATED LINKS</span></span>

[<span data-ttu-id="47b91-129">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="47b91-129">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="47b91-130">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="47b91-130">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="47b91-131">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="47b91-131">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="47b91-132">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="47b91-132">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


