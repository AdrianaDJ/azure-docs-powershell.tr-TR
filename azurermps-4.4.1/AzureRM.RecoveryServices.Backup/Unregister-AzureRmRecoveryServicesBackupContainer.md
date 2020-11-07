---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: A10DC2A2-A732-416F-9C68-6533C143AE8F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupContainer.md
ms.openlocfilehash: c5ab79ca42096ab93102be1288c772cab1ac01f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763662"
---
# <span data-ttu-id="72e41-101">Unregister-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="72e41-101">Unregister-AzureRmRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="72e41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72e41-102">SYNOPSIS</span></span>
<span data-ttu-id="72e41-103">Bir Windows sunucusunun veya başka bir kapsayıcının kasasından kaydını siler.</span><span class="sxs-lookup"><span data-stu-id="72e41-103">Unregisters a Windows Server or other container from the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72e41-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="72e41-104">SYNTAX</span></span>

```
Unregister-AzureRmRecoveryServicesBackupContainer [-Container] <ContainerBase>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72e41-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="72e41-105">DESCRIPTION</span></span>
<span data-ttu-id="72e41-106">**Unregister-AzureRmRecoveryServicesBackupContainer** cmdlet 'i, kasadan bir Windows sunucusunun veya diğer yedekleme kapsayıcısının kaydını siler.</span><span class="sxs-lookup"><span data-stu-id="72e41-106">The **Unregister-AzureRmRecoveryServicesBackupContainer** cmdlet unregisters a Windows Server or other Backup container from the vault.</span></span>
<span data-ttu-id="72e41-107">Bu cmdlet, kasadaki bir kapsayıcıya yapılan başvuruları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="72e41-107">This cmdlet removes references to a container from the vault.</span></span>
<span data-ttu-id="72e41-108">Bir kapsayıcının kaydını silebilmek için, bu kapsayıcıyla ilişkili tüm korumalı verileri silmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="72e41-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>

<span data-ttu-id="72e41-109">Geçerli cmdlet 'i kullanmadan önce Set-AzureRmRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="72e41-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="72e41-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="72e41-110">EXAMPLES</span></span>

### <span data-ttu-id="72e41-111">Örnek 1: kasadan bir Windows sunucusunun kaydını kaldırma</span><span class="sxs-lookup"><span data-stu-id="72e41-111">Example 1: Unregister a Windows Server from the vault</span></span>
```
PS C:\>$Cont = Get-AzureRmRecoveryServicesContainer -ContainerType "Windows" -BackupManagementType MARS -Name "server01.contoso.com"
PS C:\> Unregister-AzureRmRecoveryServicesBackupContainer -Container $Cont
```

<span data-ttu-id="72e41-112">İlk komut, kasaya kaydedilen server01.contoso.com adındaki Windows kapsayıcısını alır ve $Cont değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="72e41-112">The first command gets the Windows container named server01.contoso.com that is registered in the vault, and then stores it in the $Cont variable.</span></span>

<span data-ttu-id="72e41-113">İkinci komut belirtilen Windows sunucusunun kaydını Azure yedekleme kasasından siler.</span><span class="sxs-lookup"><span data-stu-id="72e41-113">The second command unregisters the specified Windows Server from the Azure Backup vault.</span></span>

## <span data-ttu-id="72e41-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="72e41-114">PARAMETERS</span></span>

### <span data-ttu-id="72e41-115">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="72e41-115">-Container</span></span>
<span data-ttu-id="72e41-116">Kaydı kaldırmak için bir yedekleme kapsayıcısı nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="72e41-116">Specifies a Backup container object to unregister.</span></span>
<span data-ttu-id="72e41-117">**Backupcontainer** nesnesi almak için Get-AzureRmRecoveryServicesBackupContainer cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="72e41-117">To obtain a **BackupContainer** object, use the Get-AzureRmRecoveryServicesBackupContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72e41-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72e41-118">-DefaultProfile</span></span>
<span data-ttu-id="72e41-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="72e41-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72e41-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72e41-120">CommonParameters</span></span>
<span data-ttu-id="72e41-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="72e41-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72e41-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72e41-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72e41-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="72e41-123">INPUTS</span></span>

## <span data-ttu-id="72e41-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="72e41-124">OUTPUTS</span></span>

## <span data-ttu-id="72e41-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="72e41-125">NOTES</span></span>

## <span data-ttu-id="72e41-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="72e41-126">RELATED LINKS</span></span>

[<span data-ttu-id="72e41-127">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="72e41-127">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)


