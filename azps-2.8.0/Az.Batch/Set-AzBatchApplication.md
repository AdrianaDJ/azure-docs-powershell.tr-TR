---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DCA1FD7A-54AF-48B1-A245-BFA9C43ACA9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchApplication.md
ms.openlocfilehash: d31c80a2da8e705c2515283ca219d05484e3c3dc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753164"
---
# <span data-ttu-id="2d7f6-101">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="2d7f6-101">Set-AzBatchApplication</span></span>

## <span data-ttu-id="2d7f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d7f6-102">SYNOPSIS</span></span>
<span data-ttu-id="2d7f6-103">Belirtilen uygulama için güncelleştirme ayarları.</span><span class="sxs-lookup"><span data-stu-id="2d7f6-103">Updates settings for the specified application.</span></span>

## <span data-ttu-id="2d7f6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2d7f6-104">SYNTAX</span></span>

```
Set-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [[-DisplayName] <String>] [[-DefaultVersion] <String>] [[-AllowUpdates] <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d7f6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2d7f6-105">DESCRIPTION</span></span>
<span data-ttu-id="2d7f6-106">**Set-AzBatchApplication** cmdlet 'ı belirtilen Azure toplu iş uygulamasının ayarlarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="2d7f6-106">The **Set-AzBatchApplication** cmdlet modifies settings for the specified Azure Batch application.</span></span>

## <span data-ttu-id="2d7f6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2d7f6-107">EXAMPLES</span></span>

### <span data-ttu-id="2d7f6-108">Örnek 1: toplu Iş hesabındaki bir uygulamayı güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="2d7f6-108">Example 1: Update an application in a Batch account</span></span>
```
PS C:\>Set-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -AllowUpdates $False
```

<span data-ttu-id="2d7f6-109">Bu komut, ContosoBatch hesabındaki Litwin uygulamasının güncelleştirmelere izin verip vermediğini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="2d7f6-109">This command changes whether the Litware application in the ContosoBatch account allows updates.</span></span>
<span data-ttu-id="2d7f6-110">Komut, uygulamanın varsayılan sürümünü veya görünen adını değiştirmez.</span><span class="sxs-lookup"><span data-stu-id="2d7f6-110">The command does not change the default version or display name of the application.</span></span>

## <span data-ttu-id="2d7f6-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2d7f6-111">PARAMETERS</span></span>

### <span data-ttu-id="2d7f6-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2d7f6-112">-AccountName</span></span>
<span data-ttu-id="2d7f6-113">Bu cmdlet 'in bir uygulamayı değiştirdiği toplu Iş hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d7f6-113">Specifies the name of the Batch account for which this cmdlet modifies an application.</span></span>

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

### <span data-ttu-id="2d7f6-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="2d7f6-114">-AllowUpdates</span></span>
<span data-ttu-id="2d7f6-115">Uygulamanın içindeki paketlerin aynı sürüm dizesini kullanarak yazılıp yazılmayacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d7f6-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d7f6-116">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="2d7f6-116">-ApplicationId</span></span>
<span data-ttu-id="2d7f6-117">Uygulamanın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d7f6-117">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="2d7f6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d7f6-118">-DefaultProfile</span></span>
<span data-ttu-id="2d7f6-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2d7f6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d7f6-120">-DefaultVersion</span><span class="sxs-lookup"><span data-stu-id="2d7f6-120">-DefaultVersion</span></span>
<span data-ttu-id="2d7f6-121">Bir istemci uygulamayı istediğinde ancak bir sürüm belirtmezse hangi paketin kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d7f6-121">Specifies which package to use if a client requests the application but does not specify a version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d7f6-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2d7f6-122">-DisplayName</span></span>
<span data-ttu-id="2d7f6-123">Uygulamanın görünen adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d7f6-123">Specifies the display name for the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d7f6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d7f6-124">-ResourceGroupName</span></span>
<span data-ttu-id="2d7f6-125">Toplu Iş hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d7f6-125">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="2d7f6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d7f6-126">CommonParameters</span></span>
<span data-ttu-id="2d7f6-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2d7f6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d7f6-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d7f6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d7f6-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2d7f6-129">INPUTS</span></span>

### <span data-ttu-id="2d7f6-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2d7f6-130">System.String</span></span>

### <span data-ttu-id="2d7f6-131">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="2d7f6-131">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="2d7f6-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2d7f6-132">OUTPUTS</span></span>

### <span data-ttu-id="2d7f6-133">System. void</span><span class="sxs-lookup"><span data-stu-id="2d7f6-133">System.Void</span></span>

## <span data-ttu-id="2d7f6-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2d7f6-134">NOTES</span></span>

## <span data-ttu-id="2d7f6-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2d7f6-135">RELATED LINKS</span></span>

[<span data-ttu-id="2d7f6-136">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="2d7f6-136">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="2d7f6-137">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="2d7f6-137">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="2d7f6-138">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="2d7f6-138">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="2d7f6-139">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="2d7f6-139">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="2d7f6-140">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="2d7f6-140">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="2d7f6-141">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="2d7f6-141">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)


