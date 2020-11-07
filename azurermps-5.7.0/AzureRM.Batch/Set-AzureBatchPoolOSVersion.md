---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 4C3C6C81-7486-4ED6-BA30-2F202E654F77
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchpoolosversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPoolOSVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPoolOSVersion.md
ms.openlocfilehash: cd21c9ce84a96ada003eb6520c9a2a115df186cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593735"
---
# <span data-ttu-id="52b83-101">Set-AzureBatchPoolOSVersion</span><span class="sxs-lookup"><span data-stu-id="52b83-101">Set-AzureBatchPoolOSVersion</span></span>

## <span data-ttu-id="52b83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52b83-102">SYNOPSIS</span></span>
<span data-ttu-id="52b83-103">Belirtilen havuzun işletim sistemi sürümünü değiştirir.</span><span class="sxs-lookup"><span data-stu-id="52b83-103">Changes the operating system version of the specified pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52b83-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="52b83-104">SYNTAX</span></span>

```
Set-AzureBatchPoolOSVersion [-Id] <String> [-TargetOSVersion] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52b83-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="52b83-105">DESCRIPTION</span></span>
<span data-ttu-id="52b83-106">**Set-AzureBatchPoolOSVersion** cmdlet 'i belirtilen havuzun işletim sistemi sürümünü değiştirir.</span><span class="sxs-lookup"><span data-stu-id="52b83-106">The **Set-AzureBatchPoolOSVersion** cmdlet changes the operating system version of the specified pool.</span></span>

## <span data-ttu-id="52b83-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="52b83-107">EXAMPLES</span></span>

### <span data-ttu-id="52b83-108">Örnek 1: bir havuzun hedef işletim sistemi sürümünü ayarlama</span><span class="sxs-lookup"><span data-stu-id="52b83-108">Example 1: Set the target operating system version of a pool</span></span>
```
PS C:\>Set-AzureBatchPoolOSVersion -Id "MyPool" -TargetOSVersion "WA-GUEST-OS-4.20_201505-01" -BatchContext $Context
```

<span data-ttu-id="52b83-109">Bu komut MyPool havuzunun hedef işletim sistemi sürümünü WA-GUEST-OS-4.20 _201505-01 olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="52b83-109">This command sets the target operating system version of pool MyPool to WA-GUEST-OS-4.20_201505-01.</span></span>

## <span data-ttu-id="52b83-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="52b83-110">PARAMETERS</span></span>

### <span data-ttu-id="52b83-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="52b83-111">-BatchContext</span></span>
<span data-ttu-id="52b83-112">Bu cmdlet 'in toplu Iş hizmetiyle etkileşimli çalışmak için kullandığı **Batchaccountcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="52b83-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="52b83-113">BatchAccountContext 'i almak için Get-AzureRmBatchAccount cmdlet 'ini kullanıyorsanız, toplu Iş hizmetiyle etkileşim kurarken Azure Active Directory kimlik doğrulaması kullanılır.</span><span class="sxs-lookup"><span data-stu-id="52b83-113">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="52b83-114">Bunun yerine paylaşılan anahtar kimlik doğrulamasını kullanmak için, Get-AzureRmBatchAccountKeys cmdlet 'ini kullanarak erişim anahtarlarının doldurulduğuna bir BatchAccountContext nesnesi alın.</span><span class="sxs-lookup"><span data-stu-id="52b83-114">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="52b83-115">Paylaşılan anahtar kimlik doğrulaması kullanırken, birincil erişim anahtarı varsayılan olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="52b83-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="52b83-116">Kullanılacak anahtarı değiştirmek için BatchAccountContext. KeyInUse özelliğini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="52b83-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52b83-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52b83-117">-DefaultProfile</span></span>
<span data-ttu-id="52b83-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="52b83-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52b83-119">-ID</span><span class="sxs-lookup"><span data-stu-id="52b83-119">-Id</span></span>
<span data-ttu-id="52b83-120">Havuzun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="52b83-120">Specifies the ID of the pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52b83-121">-TargetOSVersion</span><span class="sxs-lookup"><span data-stu-id="52b83-121">-TargetOSVersion</span></span>
<span data-ttu-id="52b83-122">Havuzdaki sanal makinelere yüklenecek Azure Konuk işletim sistemi sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="52b83-122">Specifies the Azure Guest operating system version to install on the virtual machines in the pool.</span></span>
<span data-ttu-id="52b83-123">Azure Konuk işletim sistemi sürümleri hakkında daha fazla bilgi için, bkz https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/) .</span><span class="sxs-lookup"><span data-stu-id="52b83-123">For more information on Azure Guest operating system versions, see Azure Guest OS Releases and SDK Compatibility Matrixhttps://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ (https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52b83-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52b83-124">CommonParameters</span></span>
<span data-ttu-id="52b83-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="52b83-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52b83-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52b83-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52b83-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="52b83-127">INPUTS</span></span>

### <span data-ttu-id="52b83-128">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="52b83-128">BatchAccountContext</span></span>
<span data-ttu-id="52b83-129">' BatchContext ' parametresi ardışık düzenin ' BatchAccountContext ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="52b83-129">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="52b83-130">Dizisi</span><span class="sxs-lookup"><span data-stu-id="52b83-130">String</span></span>
<span data-ttu-id="52b83-131">' ID ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="52b83-131">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="52b83-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="52b83-132">OUTPUTS</span></span>

## <span data-ttu-id="52b83-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="52b83-133">NOTES</span></span>

## <span data-ttu-id="52b83-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="52b83-134">RELATED LINKS</span></span>

[<span data-ttu-id="52b83-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="52b83-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

