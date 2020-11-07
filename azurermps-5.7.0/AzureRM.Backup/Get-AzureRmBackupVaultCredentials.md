---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9882F1A5-6FFB-4DAF-8ED5-B14596BC939D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupvaultcredentials
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVaultCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVaultCredentials.md
ms.openlocfilehash: e6e56b1b9026aa0bba4442edc9652372505983ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763587"
---
# <span data-ttu-id="b75c6-101">Get-AzureRmBackupVaultCredentials</span><span class="sxs-lookup"><span data-stu-id="b75c6-101">Get-AzureRmBackupVaultCredentials</span></span>

## <span data-ttu-id="b75c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b75c6-102">SYNOPSIS</span></span>
<span data-ttu-id="b75c6-103">Yedek Kasası için kasa kimlik bilgileri dosyasını indirir.</span><span class="sxs-lookup"><span data-stu-id="b75c6-103">Downloads the vault credentials file for a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b75c6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b75c6-104">SYNTAX</span></span>

```
Get-AzureRmBackupVaultCredentials [-TargetLocation] <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b75c6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b75c6-105">DESCRIPTION</span></span>
<span data-ttu-id="b75c6-106">**Get-AzureRmBackupVaultCredentials** cmdlet 'i, bir Azure Yedekleme Kasası için kasa kimlik bilgileri dosyasını indirir.</span><span class="sxs-lookup"><span data-stu-id="b75c6-106">The **Get-AzureRmBackupVaultCredentials** cmdlet downloads the vault credentials file for an Azure Backup vault.</span></span>

<span data-ttu-id="b75c6-107">Yedekleme, bir kasayı Azure yedekleme kasasına bağlamak ve kaydettirmek için bir kasa kimlik bilgileri dosyası kullanır.</span><span class="sxs-lookup"><span data-stu-id="b75c6-107">Backup uses a vault credential file to connect a server to the Azure Backup vault and register it.</span></span>
<span data-ttu-id="b75c6-108">Yedeklemenin kasaya yedek verileri gönderebilmek için bir sunucu kaydetmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="b75c6-108">You must register a server before Backup can send backup data to the vault.</span></span>

## <span data-ttu-id="b75c6-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b75c6-109">EXAMPLES</span></span>

## <span data-ttu-id="b75c6-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b75c6-110">PARAMETERS</span></span>

### <span data-ttu-id="b75c6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b75c6-111">-DefaultProfile</span></span>
<span data-ttu-id="b75c6-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b75c6-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b75c6-113">-TargetLocation</span><span class="sxs-lookup"><span data-stu-id="b75c6-113">-TargetLocation</span></span>
<span data-ttu-id="b75c6-114">Bu cmdlet 'in kasa kimlik bilgileri dosyasını sakladığı hedef yolu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b75c6-114">Specifies the destination path where this cmdlet stores the vault credentials file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b75c6-115">-Kasa</span><span class="sxs-lookup"><span data-stu-id="b75c6-115">-Vault</span></span>
<span data-ttu-id="b75c6-116">Bu cmdlet 'in kasa kimlik bilgileri dosyası aldığı yedek kasayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="b75c6-116">Specifies the Backup vault for which this cmdlet gets a vault credential file.</span></span>
<span data-ttu-id="b75c6-117">**Azurermbackupkasa** nesnesi almak için Get-AzureRmBackupVault cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b75c6-117">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b75c6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b75c6-118">CommonParameters</span></span>
<span data-ttu-id="b75c6-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b75c6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b75c6-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b75c6-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b75c6-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b75c6-121">INPUTS</span></span>

### <span data-ttu-id="b75c6-122">Azurermbackupkasası</span><span class="sxs-lookup"><span data-stu-id="b75c6-122">AzureRMBackupVault</span></span>

## <span data-ttu-id="b75c6-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b75c6-123">OUTPUTS</span></span>

### <span data-ttu-id="b75c6-124">Dizisi</span><span class="sxs-lookup"><span data-stu-id="b75c6-124">String</span></span>
<span data-ttu-id="b75c6-125">Bu cmdlet, kasa kimlik bilgileri dosyasının adını döndürür.</span><span class="sxs-lookup"><span data-stu-id="b75c6-125">This cmdlet returns the name of the vault credential file.</span></span>

## <span data-ttu-id="b75c6-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b75c6-126">NOTES</span></span>

## <span data-ttu-id="b75c6-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b75c6-127">RELATED LINKS</span></span>

[<span data-ttu-id="b75c6-128">Get-Azurermbackupkasası</span><span class="sxs-lookup"><span data-stu-id="b75c6-128">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


