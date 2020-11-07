---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: E2A56E55-30A3-4A2F-80AE-9D166840909E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmRemoteDesktopFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmRemoteDesktopFile.md
ms.openlocfilehash: f4b29849109959a8b06a8d0339c8927b8a840a7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762757"
---
# <span data-ttu-id="8789b-101">Get-AzureRmRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="8789b-101">Get-AzureRmRemoteDesktopFile</span></span>

## <span data-ttu-id="8789b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8789b-102">SYNOPSIS</span></span>
<span data-ttu-id="8789b-103">Bir. rdp dosyası alır.</span><span class="sxs-lookup"><span data-stu-id="8789b-103">Gets an .rdp file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8789b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8789b-104">SYNTAX</span></span>

### <span data-ttu-id="8789b-105">İndirin</span><span class="sxs-lookup"><span data-stu-id="8789b-105">Download</span></span>
```
Get-AzureRmRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [-LocalPath] <String>
 [<CommonParameters>]
```

### <span data-ttu-id="8789b-106">Başlatılması</span><span class="sxs-lookup"><span data-stu-id="8789b-106">Launch</span></span>
```
Get-AzureRmRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [[-LocalPath] <String>] [-Launch]
 [<CommonParameters>]
```

## <span data-ttu-id="8789b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8789b-107">DESCRIPTION</span></span>
<span data-ttu-id="8789b-108">**Get-AzureRmRemoteDesktopFile** cmdlet 'ı bir Uzak Masaüstü Protokolü (. rdp) dosyası alır.</span><span class="sxs-lookup"><span data-stu-id="8789b-108">The **Get-AzureRmRemoteDesktopFile** cmdlet gets a Remote Desktop Protocol (.rdp) file.</span></span>

## <span data-ttu-id="8789b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8789b-109">EXAMPLES</span></span>

### <span data-ttu-id="8789b-110">Örnek 1: uzak masaüstü dosyası alma</span><span class="sxs-lookup"><span data-stu-id="8789b-110">Example 1: Get a Remote Desktop file</span></span>
```
PS C:\> Get-AzureRmRemoteDesktopFile -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -LocalPath "D:\RemoteDesktopFile07.rdp"
```

<span data-ttu-id="8789b-111">Bu komut, VirtualMachine07 adındaki sanal makine için Uzak Masaüstü dosyasını alır.</span><span class="sxs-lookup"><span data-stu-id="8789b-111">This command gets the Remote Desktop file for the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="8789b-112">Komut, sonucu D:\remotedesktopfile07.rdpadındaki dosyada depolar.</span><span class="sxs-lookup"><span data-stu-id="8789b-112">The command stores the result in the file named D:\RemoteDesktopFile07.rdp.</span></span>

## <span data-ttu-id="8789b-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8789b-113">PARAMETERS</span></span>

### <span data-ttu-id="8789b-114">-Başlat</span><span class="sxs-lookup"><span data-stu-id="8789b-114">-Launch</span></span>
<span data-ttu-id="8789b-115">Bu cmdlet. rdp dosyasını aldıktan sonra uzak masaüstünü başlatıyor.</span><span class="sxs-lookup"><span data-stu-id="8789b-115">Indicates that this cmdlet launches Remote Desktop after it gets the .rdp file.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Launch
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8789b-116">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="8789b-116">-LocalPath</span></span>
<span data-ttu-id="8789b-117">Bu cmdlet. rdp dosyasını depolayan yerel tam yolu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8789b-117">Specifies the local full path where this cmdlet stores the .rdp file.</span></span>

```yaml
Type: String
Parameter Sets: Download
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Launch
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8789b-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="8789b-118">-Name</span></span>
<span data-ttu-id="8789b-119">Bu cmdlet 'in aldığı kullanılabilirlik kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8789b-119">Specifies the name of the availability set that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8789b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8789b-120">-ResourceGroupName</span></span>
<span data-ttu-id="8789b-121">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8789b-121">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8789b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8789b-122">CommonParameters</span></span>
<span data-ttu-id="8789b-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8789b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8789b-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8789b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8789b-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8789b-125">INPUTS</span></span>

### <span data-ttu-id="8789b-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="8789b-126">None</span></span>
<span data-ttu-id="8789b-127">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="8789b-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8789b-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8789b-128">OUTPUTS</span></span>

## <span data-ttu-id="8789b-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8789b-129">NOTES</span></span>

## <span data-ttu-id="8789b-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8789b-130">RELATED LINKS</span></span>

