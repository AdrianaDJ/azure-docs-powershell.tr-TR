---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DCA1FD7A-54AF-48B1-A245-BFA9C43ACA9B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurermbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchApplication.md
ms.openlocfilehash: 157e7a3ee0cc7ea4a80517bf98d17c05df8c7899
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587677"
---
# <span data-ttu-id="ebd31-101">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ebd31-101">Set-AzureRmBatchApplication</span></span>

## <span data-ttu-id="ebd31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebd31-102">SYNOPSIS</span></span>
<span data-ttu-id="ebd31-103">Belirtilen uygulama için güncelleştirme ayarları.</span><span class="sxs-lookup"><span data-stu-id="ebd31-103">Updates settings for the specified application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ebd31-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ebd31-104">SYNTAX</span></span>

```
Set-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [[-DisplayName] <String>] [[-DefaultVersion] <String>] [[-AllowUpdates] <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ebd31-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ebd31-105">DESCRIPTION</span></span>
<span data-ttu-id="ebd31-106">**Set-AzureRmBatchApplication** cmdlet 'ı belirtilen Azure toplu iş uygulamasının ayarlarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="ebd31-106">The **Set-AzureRmBatchApplication** cmdlet modifies settings for the specified Azure Batch application.</span></span>

## <span data-ttu-id="ebd31-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ebd31-107">EXAMPLES</span></span>

### <span data-ttu-id="ebd31-108">Örnek 1: toplu Iş hesabındaki bir uygulamayı güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="ebd31-108">Example 1: Update an application in a Batch account</span></span>
```
PS C:\>Set-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -AllowUpdates $False
```

<span data-ttu-id="ebd31-109">Bu komut, ContosoBatch hesabındaki Llitwin uygulamasının güncelleştirmelere izin verip vermediğini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="ebd31-109">This command changes whether the Llitware application in the ContosoBatch account allows updates.</span></span>
<span data-ttu-id="ebd31-110">Komut, uygulamanın varsayılan sürümünü veya görünen adını değiştirmez.</span><span class="sxs-lookup"><span data-stu-id="ebd31-110">The command does not change the default version or display name of the application.</span></span>

## <span data-ttu-id="ebd31-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ebd31-111">PARAMETERS</span></span>

### <span data-ttu-id="ebd31-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ebd31-112">-AccountName</span></span>
<span data-ttu-id="ebd31-113">Bu cmdlet 'in bir uygulamayı değiştirdiği toplu Iş hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ebd31-113">Specifies the name of the Batch account for which this cmdlet modifies an application.</span></span>

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

### <span data-ttu-id="ebd31-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="ebd31-114">-AllowUpdates</span></span>
<span data-ttu-id="ebd31-115">Uygulamanın içindeki paketlerin aynı sürüm dizesini kullanarak yazılıp yazılmayacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ebd31-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebd31-116">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="ebd31-116">-ApplicationId</span></span>
<span data-ttu-id="ebd31-117">Uygulamanın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="ebd31-117">Specifies the ID of the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebd31-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebd31-118">-DefaultProfile</span></span>
<span data-ttu-id="ebd31-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ebd31-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ebd31-120">-DefaultVersion</span><span class="sxs-lookup"><span data-stu-id="ebd31-120">-DefaultVersion</span></span>
<span data-ttu-id="ebd31-121">Bir istemci uygulamayı istediğinde ancak bir sürüm belirtmezse hangi paketin kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ebd31-121">Specifies which package to use if a client requests the application but does not specify a version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebd31-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ebd31-122">-DisplayName</span></span>
<span data-ttu-id="ebd31-123">Uygulamanın görünen adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ebd31-123">Specifies the display name for the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebd31-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebd31-124">-ResourceGroupName</span></span>
<span data-ttu-id="ebd31-125">Toplu Iş hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ebd31-125">Specifies the name of the resource group that contains the Batch account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebd31-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebd31-126">CommonParameters</span></span>
<span data-ttu-id="ebd31-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ebd31-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebd31-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebd31-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebd31-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ebd31-129">INPUTS</span></span>

### <span data-ttu-id="ebd31-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ebd31-130">None</span></span>
<span data-ttu-id="ebd31-131">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="ebd31-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ebd31-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ebd31-132">OUTPUTS</span></span>

## <span data-ttu-id="ebd31-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ebd31-133">NOTES</span></span>

## <span data-ttu-id="ebd31-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ebd31-134">RELATED LINKS</span></span>

[<span data-ttu-id="ebd31-135">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ebd31-135">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="ebd31-136">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="ebd31-136">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="ebd31-137">Yeni-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ebd31-137">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="ebd31-138">Yeni-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="ebd31-138">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="ebd31-139">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ebd31-139">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="ebd31-140">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="ebd31-140">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)


