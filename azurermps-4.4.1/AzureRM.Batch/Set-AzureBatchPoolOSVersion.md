---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 4C3C6C81-7486-4ED6-BA30-2F202E654F77
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPoolOSVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPoolOSVersion.md
ms.openlocfilehash: 23c0a68c4b517035319150caa1d4d6a3acf799cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763406"
---
# <span data-ttu-id="d23da-101">Set-AzureBatchPoolOSVersion</span><span class="sxs-lookup"><span data-stu-id="d23da-101">Set-AzureBatchPoolOSVersion</span></span>

## <span data-ttu-id="d23da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d23da-102">SYNOPSIS</span></span>
<span data-ttu-id="d23da-103">Belirtilen havuzun işletim sistemi sürümünü değiştirir.</span><span class="sxs-lookup"><span data-stu-id="d23da-103">Changes the operating system version of the specified pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d23da-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d23da-104">SYNTAX</span></span>

```
Set-AzureBatchPoolOSVersion [-Id] <String> [-TargetOSVersion] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d23da-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d23da-105">DESCRIPTION</span></span>
<span data-ttu-id="d23da-106">**Set-AzureBatchPoolOSVersion** cmdlet 'i belirtilen havuzun işletim sistemi sürümünü değiştirir.</span><span class="sxs-lookup"><span data-stu-id="d23da-106">The **Set-AzureBatchPoolOSVersion** cmdlet changes the operating system version of the specified pool.</span></span>

## <span data-ttu-id="d23da-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d23da-107">EXAMPLES</span></span>

### <span data-ttu-id="d23da-108">Örnek 1: bir havuzun hedef işletim sistemi sürümünü ayarlama</span><span class="sxs-lookup"><span data-stu-id="d23da-108">Example 1: Set the target operating system version of a pool</span></span>
```
PS C:\>Set-AzureBatchPoolOSVersion -Id "MyPool" -TargetOSVersion "WA-GUEST-OS-4.20_201505-01" -BatchContext $Context
```

<span data-ttu-id="d23da-109">Bu komut MyPool havuzunun hedef işletim sistemi sürümünü WA-GUEST-OS-4.20 _201505-01 olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d23da-109">This command sets the target operating system version of pool MyPool to WA-GUEST-OS-4.20_201505-01.</span></span>

## <span data-ttu-id="d23da-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d23da-110">PARAMETERS</span></span>

### <span data-ttu-id="d23da-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d23da-111">-BatchContext</span></span>
<span data-ttu-id="d23da-112">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d23da-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d23da-113">Aboneliğinizin erişim tuşlarını içeren bir **Batchaccountcontext** nesnesi edinmek için Get-AzureRmBatchAccountKeys cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d23da-113">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="d23da-114">-ID</span><span class="sxs-lookup"><span data-stu-id="d23da-114">-Id</span></span>
<span data-ttu-id="d23da-115">Havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d23da-115">Specifies the ID of the pool.</span></span>

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

### <span data-ttu-id="d23da-116">-TargetOSVersion</span><span class="sxs-lookup"><span data-stu-id="d23da-116">-TargetOSVersion</span></span>
<span data-ttu-id="d23da-117">Havuzdaki sanal makinelere yüklenecek Azure Konuk işletim sistemi sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="d23da-117">Specifies the Azure Guest operating system version to install on the virtual machines in the pool.</span></span>
<span data-ttu-id="d23da-118">Azure Konuk işletim sistemi sürümleri hakkında daha fazla bilgi için, bkz https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/) .</span><span class="sxs-lookup"><span data-stu-id="d23da-118">For more information on Azure Guest operating system versions, see Azure Guest OS Releases and SDK Compatibility Matrixhttps://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ (https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/).</span></span>

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

### <span data-ttu-id="d23da-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d23da-119">-DefaultProfile</span></span>
<span data-ttu-id="d23da-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d23da-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d23da-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d23da-121">CommonParameters</span></span>
<span data-ttu-id="d23da-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d23da-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d23da-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d23da-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d23da-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d23da-124">INPUTS</span></span>

### <span data-ttu-id="d23da-125">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d23da-125">BatchAccountContext</span></span>
<span data-ttu-id="d23da-126">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="d23da-126">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="d23da-127">Dizisi</span><span class="sxs-lookup"><span data-stu-id="d23da-127">String</span></span>
<span data-ttu-id="d23da-128">' ID ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="d23da-128">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="d23da-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d23da-129">OUTPUTS</span></span>

## <span data-ttu-id="d23da-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d23da-130">NOTES</span></span>

## <span data-ttu-id="d23da-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d23da-131">RELATED LINKS</span></span>

[<span data-ttu-id="d23da-132">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="d23da-132">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

