---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 2605B232-10CA-4426-9917-7C9719C15166
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/enable-azurermbackupcontainerreregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupContainerReregistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupContainerReregistration.md
ms.openlocfilehash: f64453995418df572480426e7c2c63e497cf000f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592960"
---
# <span data-ttu-id="3941b-101">Enable-AzureRmBackupContainerReregistration</span><span class="sxs-lookup"><span data-stu-id="3941b-101">Enable-AzureRmBackupContainerReregistration</span></span>

## <span data-ttu-id="3941b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3941b-102">SYNOPSIS</span></span>
<span data-ttu-id="3941b-103">Yedekleme kasasına bağlanmak için bir sunucuya kaydedin.</span><span class="sxs-lookup"><span data-stu-id="3941b-103">Reregisters a server to connect to a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3941b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3941b-104">SYNTAX</span></span>

```
Enable-AzureRmBackupContainerReregistration [-Container] <AzureRMBackupContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3941b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3941b-105">DESCRIPTION</span></span>
<span data-ttu-id="3941b-106">**Enable-AzureRmBackupContainerReregistration** cmdlet 'i bir sunucuya, bir Azure yedekleme kasasına bağlanmak ve yedekleme kurtarma noktası zincirine devam eder.</span><span class="sxs-lookup"><span data-stu-id="3941b-106">The **Enable-AzureRmBackupContainerReregistration** cmdlet reregisters a server to connect to an Azure Backup vault and continue the Backup recovery point chain.</span></span>

<span data-ttu-id="3941b-107">Bir sunucuyu bozsanız, tüm bulut yedekleme noktaları yedekleme kasasında kalır.</span><span class="sxs-lookup"><span data-stu-id="3941b-107">If you destroy a server, all its cloud backup points remain in the Backup vault.</span></span>
<span data-ttu-id="3941b-108">Yeni bir sunucu oluşturup aynı tam etki alanı adı atarsanız, sunucuyu aynı kasaya bağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3941b-108">If you create a replacement server and assign it the same fully qualified domain name, you can connect the server back to the same vault.</span></span>
<span data-ttu-id="3941b-109">Bu cmdlet, yedekleme 'yi yedekleme ve varolan kümenin yeni yedek noktalarını ekleme olanağını verir.</span><span class="sxs-lookup"><span data-stu-id="3941b-109">This cmdlet enables Backup to make backups and add new backup points to the existing set.</span></span>
<span data-ttu-id="3941b-110">Yeni sunucu yedekleme zincirinde devam eder.</span><span class="sxs-lookup"><span data-stu-id="3941b-110">The new the server continues in the backup chain.</span></span>

## <span data-ttu-id="3941b-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3941b-111">EXAMPLES</span></span>

## <span data-ttu-id="3941b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3941b-112">PARAMETERS</span></span>

### <span data-ttu-id="3941b-113">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="3941b-113">-Container</span></span>
<span data-ttu-id="3941b-114">Bu cmdlet 'in tekrar tekrar kullandığı kapsayıcıyı belirtir.</span><span class="sxs-lookup"><span data-stu-id="3941b-114">Specifies the container that this cmdlet reregisters.</span></span>
<span data-ttu-id="3941b-115">**Azurermbackupcontainer** almak için Get-AzureRmBackupContainer cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="3941b-115">To obtain an **AzureRmBackupContainer** , use the Get-AzureRmBackupContainer cmdlet.</span></span>

```yaml
Type: AzureRMBackupContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3941b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3941b-116">-DefaultProfile</span></span>
<span data-ttu-id="3941b-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3941b-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3941b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3941b-118">CommonParameters</span></span>
<span data-ttu-id="3941b-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3941b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3941b-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3941b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3941b-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3941b-121">INPUTS</span></span>

### <span data-ttu-id="3941b-122">AzureBackupContainer</span><span class="sxs-lookup"><span data-stu-id="3941b-122">AzureBackupContainer</span></span>

## <span data-ttu-id="3941b-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3941b-123">OUTPUTS</span></span>

### <span data-ttu-id="3941b-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="3941b-124">None</span></span>

## <span data-ttu-id="3941b-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3941b-125">NOTES</span></span>

## <span data-ttu-id="3941b-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3941b-126">RELATED LINKS</span></span>

[<span data-ttu-id="3941b-127">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="3941b-127">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="3941b-128">Register-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="3941b-128">Register-AzureRmBackupContainer</span></span>](./Register-AzureRmBackupContainer.md)


