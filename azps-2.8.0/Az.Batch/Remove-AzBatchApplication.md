---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2CED21D6-4BEF-423B-A04A-5B812CEB975D
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
ms.openlocfilehash: 2a449235ac2b3fa98357e91e15602a0c7bd9eedb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753169"
---
# <span data-ttu-id="f7750-101">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="f7750-101">Remove-AzBatchApplication</span></span>

## <span data-ttu-id="f7750-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7750-102">SYNOPSIS</span></span>
<span data-ttu-id="f7750-103">Bir uygulamayı toplu Iş hesabından siler.</span><span class="sxs-lookup"><span data-stu-id="f7750-103">Deletes an application from a Batch account.</span></span>

## <span data-ttu-id="f7750-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f7750-104">SYNTAX</span></span>

```
Remove-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7750-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f7750-105">DESCRIPTION</span></span>
<span data-ttu-id="f7750-106">**Remove-AzBatchApplication** cmdlet 'ı bir Azure toplu hesabından uygulamayı siler.</span><span class="sxs-lookup"><span data-stu-id="f7750-106">The **Remove-AzBatchApplication** cmdlet deletes an application from an Azure Batch account.</span></span>

## <span data-ttu-id="f7750-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f7750-107">EXAMPLES</span></span>

### <span data-ttu-id="f7750-108">Örnek 1: bir uygulamayı toplu hesaptan silme</span><span class="sxs-lookup"><span data-stu-id="f7750-108">Example 1: Delete an application from a Batch account</span></span>
```
PS C:\>Remove-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware"
```

<span data-ttu-id="f7750-109">Bu komut, ContosoBatch hesabından Litwin uygulamasını siler.</span><span class="sxs-lookup"><span data-stu-id="f7750-109">This command deletes the Litware application from the ContosoBatch account.</span></span>
<span data-ttu-id="f7750-110">Uygulama herhangi bir paket içeriyorsa komut başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="f7750-110">The command fails if the application contains any packages.</span></span>

## <span data-ttu-id="f7750-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f7750-111">PARAMETERS</span></span>

### <span data-ttu-id="f7750-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f7750-112">-AccountName</span></span>
<span data-ttu-id="f7750-113">Bu cmdlet 'in uygulamayı kaldırdığı toplu hesabın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7750-113">Specifies the name of the Batch account from which this cmdlet removes an application.</span></span>

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

### <span data-ttu-id="f7750-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="f7750-114">-ApplicationId</span></span>
<span data-ttu-id="f7750-115">Uygulamanın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7750-115">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="f7750-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7750-116">-DefaultProfile</span></span>
<span data-ttu-id="f7750-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f7750-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7750-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7750-118">-ResourceGroupName</span></span>
<span data-ttu-id="f7750-119">Toplu Iş hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f7750-119">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="f7750-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7750-120">CommonParameters</span></span>
<span data-ttu-id="f7750-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f7750-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7750-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7750-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7750-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f7750-123">INPUTS</span></span>

### <span data-ttu-id="f7750-124">System. String</span><span class="sxs-lookup"><span data-stu-id="f7750-124">System.String</span></span>

## <span data-ttu-id="f7750-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f7750-125">OUTPUTS</span></span>

### <span data-ttu-id="f7750-126">System. void</span><span class="sxs-lookup"><span data-stu-id="f7750-126">System.Void</span></span>

## <span data-ttu-id="f7750-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f7750-127">NOTES</span></span>

## <span data-ttu-id="f7750-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f7750-128">RELATED LINKS</span></span>

[<span data-ttu-id="f7750-129">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="f7750-129">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="f7750-130">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="f7750-130">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="f7750-131">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="f7750-131">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="f7750-132">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="f7750-132">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="f7750-133">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="f7750-133">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="f7750-134">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="f7750-134">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)

