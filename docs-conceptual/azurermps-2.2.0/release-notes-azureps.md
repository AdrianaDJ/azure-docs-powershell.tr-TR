---
title: Azure PowerShell Değişiklik Günlüğü | Microsoft Docs
description: Azure PowerShell'in en son sürümünde yapılan değişikliklerin geçmişi aşağıda verilmiştir.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: ca25f3c66f8e8f4c64fc04275da2bd28e32d2f6c
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/08/2018
ms.locfileid: "34854622"
---
# <a name="release-notes"></a><span data-ttu-id="b052c-103">Sürüm notları</span><span class="sxs-lookup"><span data-stu-id="b052c-103">Release notes</span></span>

<span data-ttu-id="b052c-104">Azure PowerShell'in bu sürümünde yapılan değişikliklerin listesi aşağıda verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="b052c-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="version-220"></a><span data-ttu-id="b052c-105">Sürüm 2.2.0</span><span class="sxs-lookup"><span data-stu-id="b052c-105">Version 2.2.0</span></span>
* <span data-ttu-id="b052c-106">İşlem</span><span class="sxs-lookup"><span data-stu-id="b052c-106">Compute</span></span>
  - <span data-ttu-id="b052c-107">AzureDiskEncryptionForLinux uzantısından sorgu şifreleme durumu için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="b052c-107">Add support for querying encryption status from the AzureDiskEncryptionForLinux extension</span></span>
* <span data-ttu-id="b052c-108">DataFactory</span><span class="sxs-lookup"><span data-stu-id="b052c-108">DataFactory</span></span>
  - <span data-ttu-id="b052c-109">Etkinlik pencerelerini listelemek için yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="b052c-109">Added new cmdlet for listing activity windows</span></span>
    + <span data-ttu-id="b052c-110">Get-AzureRmDataFactoryActivityWindow</span><span class="sxs-lookup"><span data-stu-id="b052c-110">Get-AzureRmDataFactoryActivityWindow</span></span>
* <span data-ttu-id="b052c-111">DataLake</span><span class="sxs-lookup"><span data-stu-id="b052c-111">DataLake</span></span>
  - <span data-ttu-id="b052c-112">`Host` parametresi `DatabaseHost` olarak değiştirildi ve `Host` parametresine diğer ad eklendi</span><span class="sxs-lookup"><span data-stu-id="b052c-112">Changed parameter `Host` to `DatabaseHost` and added alias to `Host`</span></span>
    + <span data-ttu-id="b052c-113">New-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="b052c-113">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>
    + <span data-ttu-id="b052c-114">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="b052c-114">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>
  - <span data-ttu-id="b052c-115">ACL ve varsayılan ACL kaldırma desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="b052c-115">Add support for ACL and Default ACL removal</span></span>
  - <span data-ttu-id="b052c-116">Dosya ve klasörler üzerinde adsız izinler alma ve ayarlama desteği eklendi</span><span class="sxs-lookup"><span data-stu-id="b052c-116">Add support for getting and setting unnamed permissions on files and folders</span></span>
* <span data-ttu-id="b052c-117">KeyVault</span><span class="sxs-lookup"><span data-stu-id="b052c-117">KeyVault</span></span>
  - <span data-ttu-id="b052c-118">Sertifikalar için destek eklendi</span><span class="sxs-lookup"><span data-stu-id="b052c-118">Add support for certificates</span></span>
    + <span data-ttu-id="b052c-119">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b052c-119">Add-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="b052c-120">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="b052c-120">Add-AzureKeyVaultCertificateContact</span></span>
    + <span data-ttu-id="b052c-121">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b052c-121">Get-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="b052c-122">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="b052c-122">Get-AzureKeyVaultCertificateContact</span></span>
    + <span data-ttu-id="b052c-123">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="b052c-123">Get-AzureKeyVaultCertificateIssuer</span></span>
    + <span data-ttu-id="b052c-124">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="b052c-124">Get-AzureKeyVaultCertificateOperation</span></span>
    + <span data-ttu-id="b052c-125">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="b052c-125">Get-AzureKeyVaultCertificatePolicy</span></span>
    + <span data-ttu-id="b052c-126">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b052c-126">Import-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="b052c-127">New-AzureKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="b052c-127">New-AzureKeyVaultCertificateAdministratorDetails</span></span>
    + <span data-ttu-id="b052c-128">New-AzureKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="b052c-128">New-AzureKeyVaultCertificateOrganizationDetails</span></span>
    + <span data-ttu-id="b052c-129">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="b052c-129">New-AzureKeyVaultCertificatePolicy</span></span>
    + <span data-ttu-id="b052c-130">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="b052c-130">Remove-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="b052c-131">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="b052c-131">Remove-AzureKeyVaultCertificateContact</span></span>
    + <span data-ttu-id="b052c-132">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="b052c-132">Remove-AzureKeyVaultCertificateIssuer</span></span>
    + <span data-ttu-id="b052c-133">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="b052c-133">Remove-AzureKeyVaultCertificateOperation</span></span>
    + <span data-ttu-id="b052c-134">Set-AzureKeyVaultCertificateAttribute</span><span class="sxs-lookup"><span data-stu-id="b052c-134">Set-AzureKeyVaultCertificateAttribute</span></span>
    + <span data-ttu-id="b052c-135">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="b052c-135">Set-AzureKeyVaultCertificateIssuer</span></span>
    + <span data-ttu-id="b052c-136">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="b052c-136">Set-AzureKeyVaultCertificatePolicy</span></span>
    + <span data-ttu-id="b052c-137">Stop-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="b052c-137">Stop-AzureKeyVaultCertificateOperation</span></span>
* <span data-ttu-id="b052c-138">Ağ</span><span class="sxs-lookup"><span data-stu-id="b052c-138">Network</span></span>

  - <span data-ttu-id="b052c-139">+New-AzureRmNetworkInterface -EnableAcceleratedNetworking hızlandırılmış ağ oluşturmayı etkinleştirmek/devre dışı bırakmak üzere ağ arabirimi için yeni anahtar parametresi eklendi</span><span class="sxs-lookup"><span data-stu-id="b052c-139">New switch parameter added for network interface to enable/disable accelerated networking +New-AzureRmNetworkInterface -EnableAcceleratedNetworking</span></span>
  - <span data-ttu-id="b052c-140">Etkin-Etkin ağ geçidi özelliği PowerShell cmdlet’ini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="b052c-140">Enable Active-Active gateway feature PowerShell cmdlets</span></span>
    + <span data-ttu-id="b052c-141">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="b052c-141">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
    + <span data-ttu-id="b052c-142">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="b052c-142">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="b052c-143">Yeni cmdlet eklendi</span><span class="sxs-lookup"><span data-stu-id="b052c-143">Added new cmdlet</span></span>
    + <span data-ttu-id="b052c-144">Test-AzureRmPrivateIpAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="b052c-144">Test-AzureRmPrivateIpAddressAvailability</span></span>
* <span data-ttu-id="b052c-145">Kaynaklar</span><span class="sxs-lookup"><span data-stu-id="b052c-145">Resources</span></span>
  - <span data-ttu-id="b052c-146">Sağlayıcı ve kaynak cmdlet'lerinde destek bölgeleri</span><span class="sxs-lookup"><span data-stu-id="b052c-146">Support zones in provider and resource cmdlets</span></span>
    + <span data-ttu-id="b052c-147">Get-AzureRmProvider</span><span class="sxs-lookup"><span data-stu-id="b052c-147">Get-AzureRmProvider</span></span>
    + <span data-ttu-id="b052c-148">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="b052c-148">New-AzureRmResource</span></span>
    + <span data-ttu-id="b052c-149">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="b052c-149">Set-AzureRmResource</span></span>
* <span data-ttu-id="b052c-150">Sql</span><span class="sxs-lookup"><span data-stu-id="b052c-150">Sql</span></span>
  - <span data-ttu-id="b052c-151">Sunucu düzeyinde Azure SQL tehdit algılama ilkesi yönetimine yönelik yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="b052c-151">Added new cmdlets for Azure SQL threat detection policy management at server level</span></span>
    + <span data-ttu-id="b052c-152">Get-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b052c-152">Get-AzureRmSqlServerThreatDetectionPolicy</span></span>
    + <span data-ttu-id="b052c-153">Remove-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b052c-153">Remove-AzureRmSqlServerThreatDetectionPolicy</span></span>
    + <span data-ttu-id="b052c-154">Set-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b052c-154">Set-AzureRmSqlServerThreatDetectionPolicy</span></span>
  - <span data-ttu-id="b052c-155">Sql Azure DataWarehouses için GeoBackupPolicy etkinleştirmeyi/devre dışı bırakmayı destekleyen yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="b052c-155">Added new cmdlets to support enabling/disabling GeoBackupPolicy for Sql Azure DataWarehouses</span></span>
    + <span data-ttu-id="b052c-156">Get-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="b052c-156">Get-AzureRmSqlDatabaseGeoBackupPolicy</span></span>
    + <span data-ttu-id="b052c-157">Set-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="b052c-157">Set-AzureRmSqlDatabaseGeoBackupPolicy</span></span>
  - <span data-ttu-id="b052c-158">Azure Sql Danışmanları ve Önerilen Eylem API’leri için yeni cmdlet’ler eklendi</span><span class="sxs-lookup"><span data-stu-id="b052c-158">Added new cmdlets for Azure Sql Advisors and Recommended Actions APIs</span></span>
    + <span data-ttu-id="b052c-159">Get-AzureRmSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="b052c-159">Get-AzureRmSqlDatabaseAdvisor</span></span>
    + <span data-ttu-id="b052c-160">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="b052c-160">Get-AzureRmSqlElasticPoolAdvisor</span></span>
    + <span data-ttu-id="b052c-161">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="b052c-161">Get-AzureRmSqlServerAdvisor</span></span>
    + <span data-ttu-id="b052c-162">Get-AzureRmSqlDatabaseRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="b052c-162">Get-AzureRmSqlDatabaseRecommendedActions</span></span>
    + <span data-ttu-id="b052c-163">Get-AzureRmSqlElasticPoolRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="b052c-163">Get-AzureRmSqlElasticPoolRecommendedActions</span></span>
    + <span data-ttu-id="b052c-164">Get-AzureRmSqlServerRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="b052c-164">Get-AzureRmSqlServerRecommendedActions</span></span>
    + <span data-ttu-id="b052c-165">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="b052c-165">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span></span>
    + <span data-ttu-id="b052c-166">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="b052c-166">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span></span>
    + <span data-ttu-id="b052c-167">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="b052c-167">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span></span>
    + <span data-ttu-id="b052c-168">Set-AzureRmSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="b052c-168">Set-AzureRmSqlDatabaseRecommendedActionState</span></span>
    + <span data-ttu-id="b052c-169">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="b052c-169">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>
    + <span data-ttu-id="b052c-170">Set-AzureRmSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="b052c-170">Set-AzureRmSqlServerRecommendedActionState</span></span>
