---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 4C3C6C81-7486-4ED6-BA30-2F202E654F77
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchpoolosversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPoolOSVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPoolOSVersion.md
ms.openlocfilehash: f35238b6236764cc3ea75132064aede71f715458
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93938601"
---
# <span data-ttu-id="0a72f-101">Set-AzBatchPoolOSVersion</span><span class="sxs-lookup"><span data-stu-id="0a72f-101">Set-AzBatchPoolOSVersion</span></span>

## <span data-ttu-id="0a72f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a72f-102">SYNOPSIS</span></span>
<span data-ttu-id="0a72f-103">Belirtilen havuzun işletim sistemi sürümünü değiştirir.</span><span class="sxs-lookup"><span data-stu-id="0a72f-103">Changes the operating system version of the specified pool.</span></span>

## <span data-ttu-id="0a72f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0a72f-104">SYNTAX</span></span>

```
Set-AzBatchPoolOSVersion [-Id] <String> [-TargetOSVersion] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a72f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0a72f-105">DESCRIPTION</span></span>
<span data-ttu-id="0a72f-106">**Set-AzBatchPoolOSVersion** cmdlet 'i belirtilen havuzun işletim sistemi sürümünü değiştirir.</span><span class="sxs-lookup"><span data-stu-id="0a72f-106">The **Set-AzBatchPoolOSVersion** cmdlet changes the operating system version of the specified pool.</span></span>

## <span data-ttu-id="0a72f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0a72f-107">EXAMPLES</span></span>

### <span data-ttu-id="0a72f-108">Örnek 1: bir havuzun hedef işletim sistemi sürümünü ayarlama</span><span class="sxs-lookup"><span data-stu-id="0a72f-108">Example 1: Set the target operating system version of a pool</span></span>
```
PS C:\>Set-AzBatchPoolOSVersion -Id "MyPool" -TargetOSVersion "WA-GUEST-OS-4.20_201505-01" -BatchContext $Context
```

<span data-ttu-id="0a72f-109">Bu komut MyPool havuzunun hedef işletim sistemi sürümünü WA-GUEST-OS-4.20 _201505-01 olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="0a72f-109">This command sets the target operating system version of pool MyPool to WA-GUEST-OS-4.20_201505-01.</span></span>

## <span data-ttu-id="0a72f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0a72f-110">PARAMETERS</span></span>

### <span data-ttu-id="0a72f-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="0a72f-111">-BatchContext</span></span>
<span data-ttu-id="0a72f-112">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a72f-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0a72f-113">BatchAccountContext 'i almak için Get-AzBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="0a72f-113">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="0a72f-114">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="0a72f-114">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="0a72f-115">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="0a72f-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="0a72f-116">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="0a72f-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a72f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a72f-117">-DefaultProfile</span></span>
<span data-ttu-id="0a72f-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0a72f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a72f-119">-ID</span><span class="sxs-lookup"><span data-stu-id="0a72f-119">-Id</span></span>
<span data-ttu-id="0a72f-120">Havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a72f-120">Specifies the ID of the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a72f-121">-TargetOSVersion</span><span class="sxs-lookup"><span data-stu-id="0a72f-121">-TargetOSVersion</span></span>
<span data-ttu-id="0a72f-122">Havuzdaki sanal makinelere yüklenecek Azure Konuk işletim sistemi sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a72f-122">Specifies the Azure Guest operating system version to install on the virtual machines in the pool.</span></span>
<span data-ttu-id="0a72f-123">Azure Konuk işletim sistemi sürümleri hakkında daha fazla bilgi için, bkz https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/) .</span><span class="sxs-lookup"><span data-stu-id="0a72f-123">For more information on Azure Guest operating system versions, see Azure Guest OS Releases and SDK Compatibility Matrixhttps://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ (https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a72f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a72f-124">CommonParameters</span></span>
<span data-ttu-id="0a72f-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0a72f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a72f-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a72f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a72f-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0a72f-127">INPUTS</span></span>

### <span data-ttu-id="0a72f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="0a72f-128">System.String</span></span>

### <span data-ttu-id="0a72f-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0a72f-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="0a72f-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0a72f-130">OUTPUTS</span></span>

### <span data-ttu-id="0a72f-131">System. void</span><span class="sxs-lookup"><span data-stu-id="0a72f-131">System.Void</span></span>

## <span data-ttu-id="0a72f-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0a72f-132">NOTES</span></span>

## <span data-ttu-id="0a72f-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0a72f-133">RELATED LINKS</span></span>

[<span data-ttu-id="0a72f-134">Get-Aztopluaccountkeys</span><span class="sxs-lookup"><span data-stu-id="0a72f-134">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)


