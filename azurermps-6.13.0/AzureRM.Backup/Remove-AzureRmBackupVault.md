---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 698DCD00-13C0-4C36-A74B-35215D608339
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/remove-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupVault.md
ms.openlocfilehash: 883c4a9892f4525b15369dbb1c3ed6134eb29f00
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588606"
---
# <span data-ttu-id="1849b-101">Remove-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="1849b-101">Remove-AzureRmBackupVault</span></span>

## <span data-ttu-id="1849b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1849b-102">SYNOPSIS</span></span>
<span data-ttu-id="1849b-103">Yedek Kasası siler.</span><span class="sxs-lookup"><span data-stu-id="1849b-103">Deletes a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1849b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1849b-104">SYNTAX</span></span>

```
Remove-AzureRmBackupVault [-Force] [-Vault] <AzureRMBackupVault> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1849b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1849b-105">DESCRIPTION</span></span>
<span data-ttu-id="1849b-106">**Remove-Azurermbackupkasa** cmdlet 'ı bir Azure Yedekleme Kasası siler.</span><span class="sxs-lookup"><span data-stu-id="1849b-106">The **Remove-AzureRmBackupVault** cmdlet deletes an Azure Backup vault.</span></span>
<span data-ttu-id="1849b-107">Yedek bir kasayı silebilmek için önce bu, boş olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="1849b-107">Before you can delete a Backup vault, it must be empty.</span></span>
<span data-ttu-id="1849b-108">Altyapıyı bir hizmet (IaaS) sanal makine yedekleme verileri olarak kaldırmak için **Remove-AzureRmBackupContainer** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="1849b-108">Use the **Remove-AzureRmBackupContainer** cmdlet to remove infrastructure as a service (IaaS) virtual machine backup data from the vault.</span></span>
<span data-ttu-id="1849b-109">Diğer kaydedilmiş sunucuları ve yedekleme verilerini kaldırmak için **delete-registeredserver** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="1849b-109">Use the **Delete-RegisteredServer** cmdlet to remove other registered servers and backup data.</span></span>

## <span data-ttu-id="1849b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1849b-110">EXAMPLES</span></span>

### <span data-ttu-id="1849b-111">Örnek 1: Azure Yedekleme Kasası silme</span><span class="sxs-lookup"><span data-stu-id="1849b-111">Example 1: Delete an Azure Backup vault</span></span>
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03" | Remove-AzureRmBackupVault
```

<span data-ttu-id="1849b-112">Bu komut, **Get-Azurermbackupkasa** cmdlet 'Ini kullanarak Vault03 adlı Azure Yedekleme Kasası 'nı alır.</span><span class="sxs-lookup"><span data-stu-id="1849b-112">This command gets the Azure Backup vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="1849b-113">Bu komut, ardışık düzen işlecini kullanarak bu kasayı geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="1849b-113">The command passes that vault to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1849b-114">Geçerli cmdlet Kasası kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1849b-114">The current cmdlet removes the vault.</span></span>

## <span data-ttu-id="1849b-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1849b-115">PARAMETERS</span></span>

### <span data-ttu-id="1849b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1849b-116">-DefaultProfile</span></span>
<span data-ttu-id="1849b-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="1849b-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1849b-118">-Force</span><span class="sxs-lookup"><span data-stu-id="1849b-118">-Force</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1849b-119">-Kasa</span><span class="sxs-lookup"><span data-stu-id="1849b-119">-Vault</span></span>
<span data-ttu-id="1849b-120">Bu cmdlet 'in kaldırıldığı bir yedek Kasası belirtir.</span><span class="sxs-lookup"><span data-stu-id="1849b-120">Specifies a Backup vault that this cmdlet removes.</span></span>
<span data-ttu-id="1849b-121">**Azurermbackupkasası** edinmek için Get-AzureRmBackupVault cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="1849b-121">To obtain an **AzureRmBackupVault** , use the Get-AzureRmBackupVault cmdlet.</span></span>

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

### <span data-ttu-id="1849b-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="1849b-122">-Confirm</span></span>
<span data-ttu-id="1849b-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1849b-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1849b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1849b-124">-WhatIf</span></span>
<span data-ttu-id="1849b-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1849b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1849b-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1849b-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1849b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1849b-127">CommonParameters</span></span>
<span data-ttu-id="1849b-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1849b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1849b-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1849b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1849b-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1849b-130">INPUTS</span></span>

### <span data-ttu-id="1849b-131">Microsoft. Azure. Commands. AzureBackup. modeller. Azurermbackupkasası</span><span class="sxs-lookup"><span data-stu-id="1849b-131">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>
<span data-ttu-id="1849b-132">Parametreler: kasa (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1849b-132">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="1849b-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1849b-133">OUTPUTS</span></span>

### <span data-ttu-id="1849b-134">System. void</span><span class="sxs-lookup"><span data-stu-id="1849b-134">System.Void</span></span>

## <span data-ttu-id="1849b-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1849b-135">NOTES</span></span>
* <span data-ttu-id="1849b-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1849b-136">None</span></span>

## <span data-ttu-id="1849b-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1849b-137">RELATED LINKS</span></span>

[<span data-ttu-id="1849b-138">Get-Azurermbackupkasası</span><span class="sxs-lookup"><span data-stu-id="1849b-138">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="1849b-139">Yeni-Azurermbackupkasası</span><span class="sxs-lookup"><span data-stu-id="1849b-139">New-AzureRmBackupVault</span></span>](./New-AzureRmBackupVault.md)

[<span data-ttu-id="1849b-140">Set-Azurermbackupkasası</span><span class="sxs-lookup"><span data-stu-id="1849b-140">Set-AzureRmBackupVault</span></span>](./Set-AzureRmBackupVault.md)


