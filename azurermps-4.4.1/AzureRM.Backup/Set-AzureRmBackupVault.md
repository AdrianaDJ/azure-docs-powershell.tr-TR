---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: D57C32D1-EB4F-495E-A11B-3B4066E8C552
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupVault.md
ms.openlocfilehash: 82e86d27c5ef628e6cd6122fa024ac72788e79db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592673"
---
# <span data-ttu-id="88bb4-101">Set-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="88bb4-101">Set-AzureRmBackupVault</span></span>

## <span data-ttu-id="88bb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88bb4-102">SYNOPSIS</span></span>
<span data-ttu-id="88bb4-103">Yedek kasanın depolama türünü değiştirir.</span><span class="sxs-lookup"><span data-stu-id="88bb4-103">Changes the storage type of a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88bb4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="88bb4-104">SYNTAX</span></span>

```
Set-AzureRmBackupVault [[-Storage] <AzureBackupVaultStorageType>] [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88bb4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="88bb4-105">DESCRIPTION</span></span>
<span data-ttu-id="88bb4-106">**Set-Azurermbackupkasa** cmdlet 'i, bir Azure Yedekleme Kasası depolama türünü değiştirir.</span><span class="sxs-lookup"><span data-stu-id="88bb4-106">The **Set-AzureRmBackupVault** cmdlet changes the storage type of an Azure Backup vault.</span></span>
<span data-ttu-id="88bb4-107">Kasanın diğer özelliklerini değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="88bb4-107">You cannot modify other properties of a vault.</span></span>

## <span data-ttu-id="88bb4-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="88bb4-108">EXAMPLES</span></span>

### <span data-ttu-id="88bb4-109">Örnek 1: var olan bir kasanın deposunu değiştirme</span><span class="sxs-lookup"><span data-stu-id="88bb4-109">Example 1: Change the storage for an existing vault</span></span>
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03" | Set-AzureRmBackupVault -Storage LocallyRedundant
```

<span data-ttu-id="88bb4-110">Bu komut, **Get-Azurermbackupkasa** cmdlet 'Ini kullanarak Vault03 adlı Azure Yedekleme Kasası 'nı alır.</span><span class="sxs-lookup"><span data-stu-id="88bb4-110">This command gets the Azure Backup vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="88bb4-111">Bu komut, ardışık düzen işlecini kullanarak bu kasayı geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="88bb4-111">The command passes that vault to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="88bb4-112">Geçerli cmdlet depolama türünü Locallyyedekli olarak değiştirir.</span><span class="sxs-lookup"><span data-stu-id="88bb4-112">The current cmdlet changes the storage type to LocallyRedundant.</span></span>

## <span data-ttu-id="88bb4-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="88bb4-113">PARAMETERS</span></span>

### <span data-ttu-id="88bb4-114">-Depolama</span><span class="sxs-lookup"><span data-stu-id="88bb4-114">-Storage</span></span>
<span data-ttu-id="88bb4-115">Yedekleme verileri için depolama türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="88bb4-115">Specifies the storage type for the backup data.</span></span>
<span data-ttu-id="88bb4-116">Bu parametre için kabul edilebilir değerler: Locallyyedekli ve Geoyedekli.</span><span class="sxs-lookup"><span data-stu-id="88bb4-116">The acceptable values for this parameter are: LocallyRedundant and GeoRedundant.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupVaultStorageType
Parameter Sets: (All)
Aliases: 
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88bb4-117">-Kasa</span><span class="sxs-lookup"><span data-stu-id="88bb4-117">-Vault</span></span>
<span data-ttu-id="88bb4-118">Bu cmdlet 'in değiştirdiği bir yedek Kasası belirtir.</span><span class="sxs-lookup"><span data-stu-id="88bb4-118">Specifies a Backup vault that this cmdlet modifies.</span></span>
<span data-ttu-id="88bb4-119">**Azurermbackupkasa** nesnesi almak için Get-AzureRmBackupVault cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="88bb4-119">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88bb4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88bb4-120">-DefaultProfile</span></span>
<span data-ttu-id="88bb4-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="88bb4-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88bb4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88bb4-122">CommonParameters</span></span>
<span data-ttu-id="88bb4-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="88bb4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88bb4-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88bb4-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88bb4-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="88bb4-125">INPUTS</span></span>

### <span data-ttu-id="88bb4-126">Azurermbackupkasası</span><span class="sxs-lookup"><span data-stu-id="88bb4-126">AzureRmBackupVault</span></span>

## <span data-ttu-id="88bb4-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="88bb4-127">OUTPUTS</span></span>

### <span data-ttu-id="88bb4-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="88bb4-128">None</span></span>

## <span data-ttu-id="88bb4-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="88bb4-129">NOTES</span></span>
* <span data-ttu-id="88bb4-130">Kasanın ilk sunucusunu veya sanal makinesini kaydettiğinizde, depolama türü kilitlenir.</span><span class="sxs-lookup"><span data-stu-id="88bb4-130">When you register the first server or virtual machine for a vault, the storage type is locked.</span></span> <span data-ttu-id="88bb4-131">Ardından depolama türünü değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="88bb4-131">Subsequently, you cannot change the storage type.</span></span>

## <span data-ttu-id="88bb4-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="88bb4-132">RELATED LINKS</span></span>

[<span data-ttu-id="88bb4-133">Get-Azurermbackupkasası</span><span class="sxs-lookup"><span data-stu-id="88bb4-133">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="88bb4-134">Yeni-Azurermbackupkasası</span><span class="sxs-lookup"><span data-stu-id="88bb4-134">New-AzureRmBackupVault</span></span>](./New-AzureRmBackupVault.md)

[<span data-ttu-id="88bb4-135">Remove-Azurermbackupkasası</span><span class="sxs-lookup"><span data-stu-id="88bb4-135">Remove-AzureRmBackupVault</span></span>](./Remove-AzureRmBackupVault.md)


