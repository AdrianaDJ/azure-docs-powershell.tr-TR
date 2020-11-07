---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 2CED21D6-4BEF-423B-A04A-5B812CEB975D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplication.md
ms.openlocfilehash: 357759b4e3107aaa48b363da18de74229979851a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763782"
---
# <span data-ttu-id="f221a-101">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="f221a-101">Remove-AzureRmBatchApplication</span></span>

## <span data-ttu-id="f221a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f221a-102">SYNOPSIS</span></span>
<span data-ttu-id="f221a-103">Bir uygulamayı toplu Iş hesabından siler.</span><span class="sxs-lookup"><span data-stu-id="f221a-103">Deletes an application from a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f221a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f221a-104">SYNTAX</span></span>

```
Remove-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f221a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f221a-105">DESCRIPTION</span></span>
<span data-ttu-id="f221a-106">**Remove-AzureRmBatchApplication** cmdlet 'ı bir Azure toplu hesabından uygulamayı siler.</span><span class="sxs-lookup"><span data-stu-id="f221a-106">The **Remove-AzureRmBatchApplication** cmdlet deletes an application from an Azure Batch account.</span></span>

## <span data-ttu-id="f221a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f221a-107">EXAMPLES</span></span>

### <span data-ttu-id="f221a-108">Örnek 1: bir uygulamayı toplu hesaptan silme</span><span class="sxs-lookup"><span data-stu-id="f221a-108">Example 1: Delete an application from a Batch account</span></span>
```
PS C:\>Remove-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware"
```

<span data-ttu-id="f221a-109">Bu komut, ContosoBatch hesabından Litwin uygulamasını siler.</span><span class="sxs-lookup"><span data-stu-id="f221a-109">This command deletes the Litware application from the ContosoBatch account.</span></span>
<span data-ttu-id="f221a-110">Uygulama herhangi bir paket içeriyorsa komut başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="f221a-110">The command fails if the application contains any packages.</span></span>

## <span data-ttu-id="f221a-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f221a-111">PARAMETERS</span></span>

### <span data-ttu-id="f221a-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f221a-112">-AccountName</span></span>
<span data-ttu-id="f221a-113">Bu cmdlet 'in uygulamayı kaldırdığı toplu hesabın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f221a-113">Specifies the name of the Batch account from which this cmdlet removes an application.</span></span>

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

### <span data-ttu-id="f221a-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="f221a-114">-ApplicationId</span></span>
<span data-ttu-id="f221a-115">Uygulamanın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f221a-115">Specifies the ID of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f221a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f221a-116">-ResourceGroupName</span></span>
<span data-ttu-id="f221a-117">Toplu Iş hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f221a-117">Specifies the name of the resource group that contains the Batch account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f221a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f221a-118">-DefaultProfile</span></span>
<span data-ttu-id="f221a-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f221a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f221a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f221a-120">CommonParameters</span></span>
<span data-ttu-id="f221a-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f221a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f221a-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f221a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f221a-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f221a-123">INPUTS</span></span>

## <span data-ttu-id="f221a-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f221a-124">OUTPUTS</span></span>

## <span data-ttu-id="f221a-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f221a-125">NOTES</span></span>

## <span data-ttu-id="f221a-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f221a-126">RELATED LINKS</span></span>

[<span data-ttu-id="f221a-127">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="f221a-127">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="f221a-128">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="f221a-128">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="f221a-129">Yeni-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="f221a-129">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="f221a-130">Yeni-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="f221a-130">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="f221a-131">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="f221a-131">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="f221a-132">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="f221a-132">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


